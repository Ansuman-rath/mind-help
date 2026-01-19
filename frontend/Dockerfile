# Stage 0: Install dependencies (production + build)
FROM node:20-alpine AS dependencies

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci

# --------------------------------------------------

# Stage 1: Build the Vite app
FROM node:20-alpine AS builder

WORKDIR /app

# 🔥 Inject backend URL at BUILD TIME (VERY IMPORTANT)
ARG VITE_BACKEND_URL
ENV VITE_BACKEND_URL=$VITE_BACKEND_URL

# Copy dependencies
COPY --from=dependencies /app /app

# Copy source code
COPY . .

# Build frontend
RUN npm run build

# --------------------------------------------------

# Stage 2: Nginx to serve built files
FROM nginx:stable-alpine AS deploy

# Remove default nginx config
RUN rm /etc/nginx/conf.d/default.conf

# Copy custom nginx config
COPY nginx.conf /etc/nginx/conf.d/

# Copy built frontend files
COPY --from=builder /app/dist /usr/share/nginx/html

EXPOSE 80

# Health check (optional)
HEALTHCHECK --interval=30s --timeout=10s --retries=3 \
  CMD wget -qO- http://localhost || exit 1

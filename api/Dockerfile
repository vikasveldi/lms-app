# Docker file nodejs azure app services
FROM node:20
# Create api directory
WORKDIR /api
# Install api dependencies
COPY . .
RUN npm install
# Build api
RUN npx prisma generate
RUN npm run build
# Expose port
EXPOSE 3000
# Start app
CMD [ "npm", "start" ]

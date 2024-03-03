FROM node:18
WORKDIR /submission/frontend
COPY package*.json ./
RUN npm install
COPY . .
ENV REACT_APP_BACKEND_URL=http://localhost:3000
EXPOSE 3000
RUN npm run build
CMD ["npm", "run", "start"]
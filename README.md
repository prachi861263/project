# Use an official Nginx image as the base
FROM nginx:alpine
 
# Set the maintainer label (optional)
LABEL maintainer="your-email@example.com"
 
# Copy the custom index.html into the default Nginx location
COPY index.html /usr/share/nginx/html/index.html
 echo "prachi" > /usr/share/nginx/html/index.html
# Expose port 80
EXPOSE 80
 
# Start the Nginx server
CMD ["nginx", "-g", "daemon off;"]

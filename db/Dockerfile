# Derived from official mysql image (our base image)

# Use mysql 5.7 as the flask-app is not set up to work with later versions
FROM mysql:5.7
WORKDIR /trio_task
# Add a database and root password
#in app.py
ENV MYSQL_ROOT_PASSWORD=password123 
ENV MYSQL_DATABASE=flask-db
# For hints on how to do this, consult the mysql 5.7 image documentation

# Add the content of the .sql file to your image
COPY CreateTable.sql  ./
# All scripts copied to docker-entrypoint-initdb.d/ are automatically
# executed during container startup

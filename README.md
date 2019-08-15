
```
…or create a new repository on the command line
echo "# docker-build-python" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/fzhygithub/docker-build-python.git
git push -u origin master

…or push an existing repository from the command line
git remote add origin https://github.com/fzhygithub/docker-build-python.git
git push -u origin master

…or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.



docker-build-python
DOCKER官网实例，用DOCKERFILE构建你的第一个PYTHON应用
https://www.yinyubo.cn/?p=234

#use an official Python runtime as a parent image
FROM python:2.7-slim

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]

#docker run -d -p 4000:80 python:latest
#curl http://localhost:4000
```

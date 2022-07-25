# mkdocs


## Installation

Clone the repo contents to a folder
```sh
# Open terminal in the folder containing Dockerfile
```

Creating docker image  
```sh
# $ docker build -t mkdoc:v1 .

 ---> ce6df3a2aa02
Step 3/6 : WORKDIR /docs
 ---> Running in d42e7f209943
Removing intermediate container d42e7f209943
 ---> 0dfdbf561c47
Step 4/6 : EXPOSE 8000
 ---> Running in 83c1e10a9e5b
Removing intermediate container 83c1e10a9e5b
 ---> 166bc3787a1a
Step 5/6 : ENTRYPOINT ["mkdocs"]
 ---> Running in 009d04f9f858
Removing intermediate container 009d04f9f858
 ---> 4ce99e5f59ba
Step 6/6 : CMD ["serve", "--dev-addr=0.0.0.0:8000"]
 ---> Running in 007ccf6512fa
Removing intermediate container 007ccf6512fa
 ---> 6030d511bbf3
Successfully built 6030d511bbf3
Successfully tagged mkdoc:v1
```

Remove and place the files of "setup" folder in your local directory
```sh
#example 
${pwd} = /home/test/mkdoc
```

starting container

```sh
#
docker run -d --rm -p 8000:8000 -v ${pwd}:/docs --name mkDocs mkdoc:v1
7a3cccdf89ecf7b60e4a5e25c662be44ac58b7487e9fd2fe160a44c250fc4fa9
```

This is a jbake example starter created with 'jbake -i' from jbake version 2.4. The static-site is generated with a gradle task and a docker images is created. The docker image can be used as a volume-only container together with for example an nginx server.
If you use nginx create the volume with
`docker create --name blog-data image-name` 
and start nginx with
`docker run --volumes-from blog-data -d --name myblog -p 8080:80 nginx:1.9`

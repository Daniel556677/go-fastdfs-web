FROM openjdk:8-alpine
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories  \
    && apk add --no-cache sqlite
COPY go-fastdfs.db /go-fastdfs-web/db/
COPY go-fastdfs-web.jar /go-fastdfs-web/
WORKDIR /go-fastdfs-web
EXPOSE 8088
ENTRYPOINT ["java","-jar","go-fastdfs-web.jar"]

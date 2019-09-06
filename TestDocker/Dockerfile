# 父镜像
FROM microsoft/dotnet

# 进入docker中的/usr/local/src目录
RUN cd /usr/local/src
 
# 创建mynetcore目录
RUN mkdir mynetcore

# 设置工作路径
WORKDIR /usr/local/src/mynetcore
 
# 将当前文件夹下的所有文件全部复制到工作目录
COPY *.* ./

# 设置端口
EXPOSE 8810

ENTRYPOINT ["dotnet", "TestDocker.dll", "--server.urls", "http://*:8810"]

# docker build -t mynetcore .
#docker run -it -p 8010:8810 mynetcore
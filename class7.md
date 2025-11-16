#Docker Images

Building Image:
docker build -t <imagename> -f <name of the dockerfile> <. or instance filename>

Run container:
docker run -it <imagename>

FROM : images
RUN : commands to execute when we build the image
CMD : default instructions to be executed when we run a container, can be overridden

ENTRYPOINT : default instructions to be executed when we run a container, can't be overridden

ENTRYPOINT > CMD
ENV: default variables
ADD: copy the file from local or download from internet
COPY: only copies from local
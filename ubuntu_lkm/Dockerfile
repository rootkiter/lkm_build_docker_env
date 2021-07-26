from ubuntu:focal
maintainer rootkiter@rootkiter.com

run dpkg --add-architecture i386
run apt-get update &&	apt-get install -y \
    git \
    vim

# build tool
run apt-get update &&	apt-get install -y \
    make \
    gcc \
    python3-pip

# build kernel env
run apt-get update && apt-get install -y \
    build-essential \
    libelf-dev

# kernel header
run apt-get update && apt-cache search linux-headers | \
    grep generic |grep "Linux kernel headers for" > /linux-headers.list

# example source code
COPY ../hello_ko/ /hello_ko/

run apt-get update && apt-get install -y \
    linux-headers-5.4.0-42-generic
    # linux-headers-$(uname -r)

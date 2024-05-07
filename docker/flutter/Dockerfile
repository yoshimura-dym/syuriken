FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive

ARG studio_version=2020.3.1.25
ARG flutter_version=2.5.3

RUN apt update && apt install -y \
    libglu1-mesa \
    clang \
    cmake \
    ninja-build \
    pkg-config \
    libgtk-3-dev \
    && apt-get clean \
    && echo "Downloading Flutter..." \
    && curl -sSL https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_${flutter_version}-stable.tar.xz | tar xJ -C /opt \
    && echo "Downloading Android Studio..." \
    && curl -sSL https://redirector.gvt1.com/edgedl/android/studio/ide-zips/${studio_version}/android-studio-${studio_version}-linux.tar.gz | tar xz -C /opt 
     

    
RUN echo "Creating symlinks..." && ln -s /opt/android-studio/bin/studio.sh /usr/local/bin/android_studio

RUN useradd -m user -G plugdev \
    && chown -R user:user /opt/flutter \
    && chown -R user:user /opt/android-studio

ENV PATH /opt/flutter/bin:$PATH
ENV CHROME_EXECUTABLE /usr/bin/google-chrome

ENV DEBIAN_FRONTEND newt

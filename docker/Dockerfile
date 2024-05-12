FROM centos:7

RUN yum install epel-release -y && yum update -y
#RUN rpm --import http://li.nux.ro/download/nux/RPM-GPG-KEY-nux.ro \
#    &&  rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm

## https://mirrors.tencent.com/help/centos.html
#RUN yum -y install wget
## 切换yum源
#RUN mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup \
#    && wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo


RUN yum -y install ffmpeg mediainfo zbar-devel tesseract librtmp-devel \
    && yum clean all

RUN yum update -y && yum install -y \
    git-lfs \
    cmake \
    make \
    libtool \
    autoconf \
    automake \
    nasm \
    opus-devel \
    gcc-c++ \
    # 其他依赖项
    && yum clean all

RUN git lfs install
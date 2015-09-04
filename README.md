
**下载FFMPEG和libx264的包**

ffmpeg-2.4.1.tar.bz2
last_x264.tar.bz2

自动:        **(无权限给sudo)**
1.
libx264需要yasm,所以先安装yasm
apt-get install yasm

2.
然后安装libx264
aptitude install libx264-dev 

手动:
1.
解压缩libx264
tar -xjvf last_x264.tar.bz2 

2.
安装libx264
./configure --enable-shared --enable-pic  
make  
make install  

**安装ffmpeg依赖包**

1.libfaac
aptitude install libfaac-dev

2.libmp3lame
aptitude install libmp3lame-dev  

3.libtheora
aptitude install libtheora-dev 

4.libvorbis
aptitude install libvorbis-dev

5.libxvid
aptitude install libxvidcore-dev 

6.libxext
aptitude install libxext-dev

7.libxfixes
aptitude install libxfixes-dev 

**依赖包安装完后,安装ffmpeg**

1.
先解压缩ffmpeg
tar -xjvf ffmpeg-2.4.1.tar.bz2  

2.
编译安装
./configure --prefix=/usr/local/ffmpeg --enable-gpl --enable-version3 --enable-nonfree --enable-postproc --enable-pthreads --enable-libfaac --enable-libmp3lame --enable-libtheora --enable-libx264 --enable-libxvid --enable-x11grab --enable-libvorbis  

3.over
make  
make install  

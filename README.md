# MyApplication

PahoMqttActivity为测试的Activity
res/raw中需要加三个证书文件，三个文件分别为AmazonRootCA1，private.pem.key, cert.pem.crt文件，写进入后，文件名需要改为小写字母，不能有其他字符，
证书在PahoMqttActivity中178行initCert()方法中初始化，
代码需要重写SSLSocketFactory，来读取raw中的三个证书文件，基于'org.bouncycastle:bcpkix-jdk15on:1.59'写；
mqtt client为paho-mqtt
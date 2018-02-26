GAN_mnist
==============
An example of GAN using MNIST data  
--------------  
**This is almost a copy of [golbin's GAN example: 01 - GAN.py](https://github.com/golbin/TensorFlow-Tutorials/tree/master/09%20-%20GAN).**
  
### the GAN structure:  
![image](https://github.com/Menglinucas/GAN_mnist/blob/master/GAN.PNG)  
### Notes:
>(1) 需要训练两个网络G和D  
>(2) Real Images(x) 和 Fake Images(G(z)) 维度相同  
>(3) loss function
>>D_gene = discriminator(G(z))  z为噪声输入，G(z)标签为0  
>>D_real = discriminator(x)   x图片输入，x标签为1  
>>loss_D = tf.reduce_mean(tf.log(D_real) + tf.log(1 - D_gene))  
>>loss_G = tf.reduce_mean(tf.log(D_gene))

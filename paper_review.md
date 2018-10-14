# "Paper Review : Generative Adversarial Text to Image Synthesis "

#### abstract

- ##### text를 이용한 image 생성 network
- ##### text feature와 image간의 연결고리를 증명하는 논문

#### Background
- ##### Generative adversarial network

  generator와 discriminator간의 경쟁을 통해서 우수한 sampling을 추출한다.
  
  ![GAN](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQvWEw5lVqYeUxFeMahhzGAnkF1wHuMzR0hOO6kOczGkAXNsDx0)
  
    #### generator
    
    ``` python
    def generator(input_z, input_txt=None, is_train=True, reuse=False, batch_size=batch_size):
      return net_ho, logits 
    ```
    #### discriminator
    
    ``` python
    def discriminator_x(input_images, input_txt=None, is_train=True, reuse=False):
       return net_ho
    ```
    
  
- ##### Deep symmetric structured joint embedding

    RNN network를 이용하여, sentence embedding을 진행한다.

    ``` python
    def rnn_embed(input_seqs, is_train=True, reuse=False, return_embed=False):
        if return_h3:
            return net_h4, net_h3
        else:
            return net_h4
    '''
#### Method
- Network architecture

![network_architecture](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR0EGCG-Phmg-L2RWG9ky9uBCR7Hp5GidXinDUjXXQ9r5tfG3H4Fw)

Generator : R^z*R*T-> R^D

Discriminator : R^D*R^T -> {0,1}

- Matching-aware discriminator

	- conditional GAN을 학습시킬때, (text, image) pair로 학습시키고 이 pair가 real인지 fake인지  구분하도록 학습시킨다면, 너무나 naive한 가정아래 학습을 시킨 것이다.
	- 왜냐하면 구분자는 text의 embeding와 image가 서로 대응한다는 것을 학습할 수 없기 때문이다. 
	- Real image와 mismatch된 text를 추가하여 학습하는 과정에서 image text 매칭을 학습시킨다.(구분자는 fake로 구분하여야 한다.)


  알고리즘
  1.
  2.
  3.
  4.
  5.
  6.
  
 
- Learning with manifold interpolation

- Inverting the generator for style transfer

##### reference 
- [paper link] : (https://arxiv.org/abs/1605.05396)
- [github link] : (https://github.com/zsdonghao/text-to-image)




# Building ResNet34 and ResNet50 models using Tensorflow(TF) from scratch

### Building a Residual Network

Residual networks solve degradation problem by shortcuts or skip connections, by short circuiting shallow layers to deep layers. We can stack Residual blocks more and more, without degradation in performance. This enables very deep networks to be built.

In ResNets, a "shortcut" or a "skip connection" allows the model to skip layers:  

<div style="text-align:center;">
    <img src="/Images/skip_connection_kiank.png" alt="Plant Village" width="500">
    <br>
    <caption><center> <u> <font color='purple'> <b> </b> </u><font color='purple'> <b>A ResNet block showing a skip-connection</b> </center></caption>
</div>


The image on the left shows the "main path" through the network. The image on the right adds a shortcut to the main path. By stacking these ResNet blocks on top of each other, you can form a very deep network. 

The lecture mentioned that having ResNet blocks with the shortcut also makes it very easy for one of the blocks to learn an identity function. This means that you can stack on additional ResNet blocks with little risk of harming training set performance.  
    
On that note, there is also some evidence that the ease of learning an identity function accounts for ResNets' remarkable performance even more than skip connections help with vanishing gradients.

Two main types of blocks are used in a ResNet, depending mainly on whether the input/output dimensions are the same or different. You are going to implement both of them: the "identity block" and the "convolutional block."

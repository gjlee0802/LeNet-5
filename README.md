# LeNet-5 (MNIST) and Sharpness Aware Minimization

### Introduce
We performed a task on LeNet-5 in SSU deep learning programming and hands-on classes.  
The challenge topic was to think about how to improve the performance of LeNet-5.  
I thought generalization-ability was also an important indicator to evaluate the performance of the model.  
I've seen previous studies that the sharpness of loss landscape affects the performance of generalization,  
and I studied how to increase the performance of generalization by applying Sharpness Aware Minimization on LeNet-5.  

### Performance
- Basic LeNet-5 accuracy
  * TEST 1. Pure dataset : **98.75%**
  * TEST 2. Gaussian Noise dataset(standard deviation : 0.4) : **91.62%**
  * TEST 3. Gaussian Noise dataset(standard deviation : 0.6) : **89.04%**
  * TEST 4. Gaussian Noise dataset(standard deviation : 0.8) : **86.43%**
- LeNet-5 with SAM(Sharpness-aware minimization) accuracy
  * TEST 1. Pure dataset : **99%**
  * TEST 2. Gaussian Noise dataset(standard deviation : 0.4) : **98.60%**
  * TEST 3. Gaussian Noise dataset(standard deviation : 0.6) : **98.11%**
  * TEST 4. Gaussian Noise dataset(standard deviation : 0.8) : **97.23%**

Random seeding was specified when applying Gaussian noise.  
In the case of the base LeNet-5, we show severe performance degradation on the Noise-applied Test dataset.  
On the other hand, the improved version LeNet-5 with Sharpness-aware minimization shows a slight performance degradation on the Noise-enabled Test dataset, which is even better in generalization performance.  


### Reference
Sharpness-aware minimization is a way to improve generalization performance. Check out the paper below.  
- [Pierre Foret, Ariel Kleiner, Hossein Mobahi, and Behnam Neyshabur. Sharpness-aware minimization for efficiently improving generalization. In International Conference on Learning
Representations, 2021.](https://arxiv.org/pdf/2010.01412.pdf)  

- [SAM: Sharpness-Aware Minimization (PyTorch)](https://github.com/davda54/sam)  

You can find a summary of Sharpness-aware minimization below.  
- https://github.com/gjlee0802/publications_summary/blob/main/Sharpness-Aware_Minimization_for_Efficiently_Improving_Generalization.md  
- https://github.com/gjlee0802/publications_summary/blob/main/generalization_bounds.md  

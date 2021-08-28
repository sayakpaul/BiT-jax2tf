# BiT-jax2tf
This repository hosts the code to port NumPy model weights of BiT-ResNets [1] to TensorFlow SavedModel format. These models
are results of [2]. The original model weights come from [3]. 

Huge thanks to [Willie Gierke](https://ch.linkedin.com/in/willi-gierke) (of Google) for helping with the porting. 

The TensorFlow SavedModels are available on TensorFlow Hub as a collection: https://tfhub.dev/sayakpaul/collections/bit-resnet/1. A total of 8 models are available:

|  Model <br>Name 	| Input<br>Resolution 	|                                 Classifier                                 	|                            Feature<br>Extractor                            	|
|:---------------:	|:-------------------:	|:--------------------------------------------------------------------------:	|:--------------------------------------------------------------------------:	|
| BiT-ResNet152x2 	|         384         	|  [Link](https://tfhub.dev/sayakpaul/bit_resnet152x2_384_classification/1)  	|   [Link](https://tfhub.dev/sayakpaul/bit_r152x2_384_feature_extraction/1)  	|
| BiT-ResNet152x2 	|         224         	|  [Link](https://tfhub.dev/sayakpaul/bit_resnet152x2_224_classification/1)  	|   [Link](https://tfhub.dev/sayakpaul/bit_r152x2_224_feature_extraction/1)  	|
|  BiT-ResNet50x1 	|         224         	| [Link](https://tfhub.dev/sayakpaul/distill_bit_r50x1_224_classification/1) 	| [Link](https://tfhub.dev/sayakpaul/distill_bit_r50x1_224_classification/1) 	|
|  BiT-ResNet50x1 	|         160         	| [Link](https://tfhub.dev/sayakpaul/distill_bit_r50x1_160_classification/1) 	| [Link](https://tfhub.dev/sayakpaul/distill_bit_r50x1_160_classification/1) 	|

You could use the `convert_jax_weights_tf.ipynb` notebook to understand how model porting works between JAX and TensorFlow. There
is also an experimental tool called `jax2tf` from the JAX team that you can find [here](https://github.com/google/jax/blob/main/jax/experimental/jax2tf/README.md).

## References

[1] [Big Transfer (BiT): General Visual Representation Learning by Kolesnikov et al.](https://arxiv.org/abs/1912.11370)

[2] [Knowledge distillation: A good teacher is patient and consistent by Beyer et al.](https://arxiv.org/abs/2106.05237)

[3] [BiT GitHub](https://github.com/google-research/big_transfer)

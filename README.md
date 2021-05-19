# tf-keras-applications-cifar10-example
Tensorflow Keras applicationsを用いてCIFAR10を学習する例です。<br><br>
<img src="https://user-images.githubusercontent.com/37477845/118831622-dfbd6c00-b8fa-11eb-8a72-1b54f473418c.png" width="800px"><br>
以下のモデルで試していますが、tf_keras_applications[]内の任意のモデルのコメントアウトを解除することで学習できます。
* DenseNet121
* EfficientNetB0
* MobileNet
* MobileNetV2
* NASNetMobile
* ResNet50V2

# Requirement 
* TensorFlow 2.4.0 or later

# Prerequisites
* 各モデルの入力サイズ等の設定値はデフォルト値を使用
* CIFAR10の入力サイズ(32x32)からtf.image.resize()で各モデルの入力サイズにリサイズして使用
* エポック数は25
* 最適化アルゴリズムはSGD
* 学習時のバッチサイズはデフォルト値(32)
* 出力層はFlatten()→Dense(10, activation='softmax')を接続

# Usage
tf-keras-applications-cifar10.ipynb を上から順に実行してください。

# Example
| モデル         | パラメータ数 | Loss(25エポック終了時) | Accuracy(25エポック終了時) | 
| -------------- | ------------ | ---------------------- | -------------------------- | 
| DenseNet121    | 7,539,274    | 32.90                  | 0.743                      | 
| EfficientNetB0 | 4,676,781    |  2.58                  | 0.537                      | 
| MobileNet      | 3,730,634    | 0.33                   | 0.939                      | 
| MobileNetV2    | 2,885,194    | 0.40                   | 0.934                      | 
| NASNetMobile   | 4,787,166    | 0.23                   | 0.959                      | 
| ResNet50V2     | 24,568,330   | 0.28                   | 0.950                      | 

<img src="https://user-images.githubusercontent.com/37477845/118831779-0380b200-b8fb-11eb-8607-d0c6a58b8138.png" width="800px"><br>
<img src="https://user-images.githubusercontent.com/37477845/118831793-067ba280-b8fb-11eb-86ea-371150b82450.png" width="800px"><br>
<img src="https://user-images.githubusercontent.com/37477845/118831798-07143900-b8fb-11eb-86f8-93474a9cb545.png" width="800px"><br>
<img src="https://user-images.githubusercontent.com/37477845/118831804-08456600-b8fb-11eb-8f5c-9ea53d613fd7.png" width="800px"><br>
<img src="https://user-images.githubusercontent.com/37477845/118831809-08456600-b8fb-11eb-845b-c2522c8d5747.png" width="800px"><br>
<img src="https://user-images.githubusercontent.com/37477845/118831812-09769300-b8fb-11eb-8e52-c6eb308eb4f2.png" width="800px"><br>

# Author
高橋かずひと(https://twitter.com/KzhtTkhs)
 
# License 
tf-keras-applications-cifar10-example is under [Apache-2.0 License](LICENSE).

[Japanese/[English](https://github.com/Kazuhito00/AprilTag-Detection-Python-Sample//blob/main/README_EN.md)]

# AprilTag-Detection-Python-Sample
[AprilTag](https://april.eecs.umich.edu/software/apriltag)のPythonでの検出サンプルです。<br>
検出には[pupil-labs/apriltags](https://github.com/pupil-labs/apriltags)を利用しています。<br>
※Windows以外の環境の場合は、[AprilRobotics/apriltag](https://github.com/AprilRobotics/apriltag)、[duckietown/lib-dt-apriltags](https://github.com/duckietown/lib-dt-apriltags)を利用しても構いません

https://user-images.githubusercontent.com/37477845/134534255-85189b37-e89b-44fb-9486-80153df037cf.mp4

# Requirement 
* opencv-python 4.5.3.56 or later
* pupil-apriltags 1.0.4 or later

pupil-apriltagsはpipでインストールできます。
```bash
pip install pupil-apriltags
```

# Tags
タグ画像は以下から入手してください。
* [AprilRobotics/apriltag-imgs](https://github.com/AprilRobotics/apriltag-imgs)
* [rgov/apriltag-pdfs](https://github.com/rgov/apriltag-pdfs

PDF化したものを[pdf](https://github.com/Kazuhito00/AprilTag-Detection-Sample/tree/main/pdf)ディレクトリにも格納しています

# Demo
デモの実行方法は以下です。
```bash
python sample.py
```
* --device<br>
カメラデバイス番号の指定<br>
デフォルト：0
* --width<br>
カメラキャプチャ時の横幅<br>
デフォルト：960
* --height<br>
カメラキャプチャ時の縦幅<br>
デフォルト：540
* --families<br>
タグファミリー<br>
複数指定する場合はスペース区切りで指定<br>
デフォルト：tag36h11
* --nthreads<br>
スレッド数<br>
デフォルト：1
* --quad_decimate<br>
矩形検出を間引いて速度を上げる(精度は下がる)<br>
1.0を指定した場合はフル解像度<br>
デフォルト：2.0
* --quad_sigma<br>
ガウスぼかしを適用するか否か<br>
設定値はピクセル単位の標準偏差を示す<br>
非常にノイズの多い画像は、ゼロ以外の値(0.8等)を設定することで改善する可能性がある<br>
デフォルト：0.0
* --refine_edges<br>
各矩形のエッジはを近くの強い勾配に寄せるか否か<br>
デフォルト：1
* --decode_sharpening<br>
デコードされた画像をどの程度先鋭化するか<br>
デフォルト：0.25
* --debug<br>
デバッグ画像を保存するか否か<br>
デフォルト：0

※各オプションの詳細は[pupil-labs/apriltags#usage](https://github.com/pupil-labs/apriltags#usage)を参照ください

# Reference
* [AprilTag](https://april.eecs.umich.edu/software/apriltag)
* [pupil-labs/apriltags](https://github.com/pupil-labs/apriltags)

# Author
高橋かずひと(https://twitter.com/KzhtTkhs)
 
# License 
AprilTag-Detection-Python-Sample is under [MIT License](LICENSE).

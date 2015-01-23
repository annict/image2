# Annict::Image2

## 環境

* Ubuntu 14.04


## インストールされるもの

* ImageMagick
* Nginx
* ngx_small_light


## 動かし方

```
$ git clone git@github.com:annict/image2.git
$ cd image
$ vagrant up
$ cp development{.example,} && cp group_vars/development{.example,}
$ ansible-playbook -i development site.yml
```


## サムネイル画像を作る

```
http://192.168.33.11/350x200/ald.png
http://192.168.33.11/350x200c/ald.png
http://192.168.33.11/350x200/ald.png?blur=0x5
```


## TODO

* `env OMP_NUM_THREADS=1;` を設定する
  * https://github.com/cubicdaiya/ngx_small_light#optimizing-tips
* S3にアクセスできるようにする

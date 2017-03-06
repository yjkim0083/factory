# Tensorflow

### Tensorflow 실행방법
- IP : 192.168.0.102
- 계정정보
    - root / **** (계정이 필요하면 만들어서 사용)
- 사용방법
    - CUDA 사용을 위해 LD_LIBRARY_PATH 설정
        - `export LD_LIBRARY_PATH=/usr/local/cuda/lib64`
    - Tensorflow 사용을 위해 virtualenv를 activate
        - `source /DATA/tensorenv/bin/activate`
    - Tensorflow import 확인(CUDA 라이브러리에 대한 메세지가 정상적으로 뜨는지 확인)
    ```python
    tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcublas.so.8.0 locally
    tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcudnn.so.5 locally
	tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcufft.so.8.0 locally
	tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcuda.so.1 locally
	tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcurand.so.8.0 locally
    ```

- 실행 예제
    ```shell
    yjkim@pt2-works:~$ export LD_LIBRARY_PATH=/usr/local/cuda/lib64
    yjkim@pt2-works:~$ source /DATA/tensorenv/bin/activate #virtualenv 환경 진입
    (tensorenv) yjkim@pt2-works:~$
    (tensorenv) yjkim@pt2-works:~$ python
    Python 2.7.12 (default, Nov 19 2016, 06:48:10)
    [GCC 5.4.0 20160609] on linux2
    Type "help", "copyright", "credits" or "license" for more information.
    >>> import tensorflow as tf
    I tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcublas.so.8.0 locally
    I tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcudnn.so.5 locally
    I tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcufft.so.8.0 locally
    I tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcuda.so.1 locally
    I tensorflow/stream_executor/dso_loader.cc:135] successfully opened CUDA library libcurand.so.8.0 locally
    >>> quit()
    (tensorenv) yjkim@pt2-works:~$ deactivate # virtualenv 환경 나가기
    yjkim@pt2-works:~$
    ```

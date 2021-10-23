1.windows 11설치
 - pc 상태검사 앱 다운로드 후 상태확인
```bash
https://aka.ms/GetPCHealthCheckApp
```
 - 윈도우 11 installer 다운로드 후 설치
 ```bash
 https://go.microsoft.com/fwlink/?linkid=2171764
 ```
2. windows 11 설치 후 wsl을 이용하여 터미널 창 실행
![image](https://user-images.githubusercontent.com/53217819/138554378-6c74bb31-b25d-43f3-aba6-d176dc62e9af.png)

3. NVIDIA 드라이버 및 CUDA 설치 방법
 - 참고 : https://docs.nvidia.com/cuda/wsl-user-guide/index.html
 - 주소에서 CUDA 드라이버를 다운받고 설치 https://developer.nvidia.com/cuda/wsl/download
 - 설치 후 컴퓨터 재시작
 ![image](https://user-images.githubusercontent.com/53217819/138554486-2c628817-f8de-4d97-95eb-22afdb8c2ab9.png)

 - wsl 창을 열고 다음의 명령어를 입력하여 드라이버 설치
 ```bash
 wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-ubuntu2004.pin
 sudo mv cuda-ubuntu2004.pin /etc/apt/preferences.d/cuda-repository-pin-600
 wget https://developer.download.nvidia.com/compute/cuda/11.4.0/local_installers/cuda-repo-ubuntu2004-11-4-local_11.4.0-470.42.01-1_amd64.deb
 sudo dpkg -i cuda-repo-ubuntu2004-11-4-local_11.4.0-470.42.01-1_amd64.deb
 sudo apt-key add /var/cuda-repo-ubuntu2004-11-4-local/7fa2af80.pub
 sudo apt-get update
 sudo apt-get install -y cuda-toolkit-11-4
 ```
 - nvidia-smi를 통해 확인
 ```bash
 nvidia-smi
 ```
![image](https://user-images.githubusercontent.com/53217819/138554608-6c2fd592-0cb8-482e-80e7-b7f9c41bc1fc.png)

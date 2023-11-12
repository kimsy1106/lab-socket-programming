#DevOps Example

##### Node.js , npm 설치가 되어있어야 함.
    
    sudo apt install npm

##### pm2 설치

    npm install -g pm2

##### settings > webhooks 설정

![image](https://github.com/kimsy1106/lab-socket-programming/assets/53938323/eab68eb3-c7f3-459a-b295-19015afca2da)



##### webhooks.py 와 tcp-server.py 실행

    pm2 start webhooks.py --name webhooks --interpreter python3

    pm2 start tcp-server.py --name tcp-server --interpreter python3 --watch        << watch 옵션 : 소스코드가 변경되면 재가동

![image](https://github.com/kimsy1106/lab-socket-programming/assets/53938323/819cb8c1-880d-4081-8ce2-2f46a13c004f)


##### tcp-server.py 수정 및 변경 적용 확인

    - local repository

    tcp-server.py 코드 일부 수정 후,

    git add .
    git commit -m "commit message"
    git push

    - cloud 

     more tcp-server.py   << 변경 적용 확인

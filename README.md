#DevOps Example

##### Node.js , npm 설치가 되어있어야 함.
    
    sudo apt install npm

##### pm2 설치

    npm install -g pm2

##### webhooks.py 와 tcp-server.py 실행

    pm2 start webhooks.py --name webhooks --interpreter python3

    pm2 start tcp-server.py --name tcp-server --interpreter python3 --watch        << watch 옵션 : 소스코드가 변경되면 재가동

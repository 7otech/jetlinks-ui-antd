cnpm install
npm run build

cp -r dist docker/

sudo docker build -t registry.cn-shenzhen.aliyuncs.com/jetlinks/jetlinks-ui-antd:$(node -p "require('./package.json').version") ./docker

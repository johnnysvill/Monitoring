# Monitoring

Этот проект настраивает мониторинг веб-сайтов с использованием Prometheus и Blackbox Exporter. Prometheus собирает метрики с Blackbox Exporter, который проверяет доступность веб-сайта ptsecurity.com.

Для развертывания проекта необходимо:
1. Установить docker-compose:
```bash
sudo apt-get update
sudo apt-get install -y curl
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```
2. Установить docker:
```bash
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
echo "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list
sudo apt update
sudo apt install docker-ce -y
```
3. Клонировать репозиторий и войти в директорию репозитория:
```bash
git clone https://github.com/johnnysvill/Monitoring.git
cd Monitoring
```
4. Запустить проект с помощью команды:
```bash
docker-compose up -d
```
5. Проверка работы:
```bash
Доступ к интерфейсу Prometheus: http://localhost:9090
Доступ к Blackbox Exporter: http://localhost:9115
```


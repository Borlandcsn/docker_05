Домашнее задание к занятию 5. «Практическое применение Docker»

Задача 0

![Screenshot_1](https://github.com/user-attachments/assets/c6640921-caa8-4e2e-abb2-e925e0d90584)

Задача 1

https://github.com/Borlandcsn/shvirtd-example-python

![Screenshot_11](https://github.com/user-attachments/assets/85d3ff3d-a798-4dc9-867f-4cd8b7c988c3)

Задача 2

![Screenshot_1](https://github.com/user-attachments/assets/1c5d955f-3fcb-4a1f-b585-f38de69e157a)

Задача 3

![Screenshot_5](https://github.com/user-attachments/assets/cc442de1-9d1e-4166-9cb2-49538d459e02)


![Screenshot_1](https://github.com/user-attachments/assets/38cf3974-40ad-4ff3-8072-37e14f5ae82e)

Задача 4

![Screenshot_2](https://github.com/user-attachments/assets/80150c48-c333-431e-a2ed-568c84cdc100)

![Screenshot_1](https://github.com/user-attachments/assets/87b6acc9-4557-485f-a325-bd62eb062913)

https://github.com/Borlandcsn/shvirtd-example-python.git

Задача 6

#устанавливаем dive 

DIVE_VERSION=$(curl -sL "https://api.github.com/repos/wagoodman/dive/releases/latest" | grep '"tag_name":' | sed -E 's/.*"v([^"]+)".*/\1/')

curl -OL https://github.com/wagoodman/dive/releases/download/v${DIVE_VERSION}/dive_${DIVE_VERSION}_linux_amd64.deb

sudo apt install ./dive_${DIVE_VERSION}_linux_amd64.deb

изучаем образ с помощью dive и находим нас интересующий слой

![Screenshot_2](https://github.com/user-attachments/assets/4e0b2460-aee7-4ff6-bb95-83fd45e829da)

docker save hashicorp/terraform:latest -o terraform_image.tar

mkdir layers

tar -xf terraform_image.tar -C layers/

cd layers/blobs/sha256/

tar -xf 39d97dd55629c8aba7fbcc9677c5b82aa7acde6a64767eb542c4dad181acd556

cd bin

cp terraform ~/

![Screenshot_1](https://github.com/user-attachments/assets/217fe6e8-1b7e-489b-8f05-74f3fff10d78)

Задание 6.1

Добейтесь аналогичного результата, используя docker cp.

Предоставьте скриншоты действий .

![Screenshot_3](https://github.com/user-attachments/assets/ec2d7cbf-5f53-45a3-add5-955386c90621)




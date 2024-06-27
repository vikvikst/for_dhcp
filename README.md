# for_dhcp

1) Загрузите образ на локальную машину
docker pull vikvikst/for_dhcp
2)Скопируйте директорию result, которая содержит файл базы данных
3) Задайте владельца директории result
chown -R root:root result/
4) Соберите и запустите контейнер на удобном для вас порту, гуникорн слушает 5000
docker run -v $(pwd)/result:/for_dhcp/result --name for_dhcp -d -p 8000:5000 vikvikst/for_dhcp 

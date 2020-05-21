# Вторая часть Git
### Git clone 
Для того чтобы скачать твои файлы с другого компьютера, нужно ввести команду **git clone <url>**, где url это ссылка на твой проект, выглядит он примерно так:  
**git clone https://github.com/sakenism/test.git**   
Очевидно, перед скачиванием git попросит твои данные - user.name, password.  
    
   
### Откат к старой версии
    
Если по какой-то причине тебе нужно откатиться на одну из прошлых версий своего проекта, нужно сделать следующие операции:   
- **git log** для того, чтобы узнать хэш твоего старого коммита, выглядит он примерно так - 12345678901234567890123456789012345678ab
- **git checkout commit_hash** вместо commit_hash вставляешь хэш коммита который тебе нужен, поздравляю, теперь ты видишь свой старый код.

<iframe width="560" height="315" src="https://www.youtube.com/embed/RIYrfkZjWmA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>  


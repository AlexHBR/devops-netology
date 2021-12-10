#Домашнее задание к занятию «2.4. Инструменты Git»#
2. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea?  
`>git show aefea`  
    >aefead2207ef7e2aa5dc81a34aedf0cad4c32545  
    Update CHANGELOG.md  
	 
3. Какому тегу соответствует коммит 85024d3?  
`>git show 85024`  
    >commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)  

4. Сколько родителей у коммита b8d720? Напишите их хеши.
`>git show --pretty=format:" %P" b8d720`
    >56cd7859e05c36c06b56d013b55a252d0bb7e158 9ea88f22fc6269854151c571162c5bcf958bee2b
 
5. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.  
`>git log  v0.12.23..v0.12.24  --oneline`
    >33ff1c03b (tag: v0.12.24) v0.12.24  
    b14b74c49 [Website] vmc provider links  
    3f235065b Update CHANGELOG.md  
    6ae64e247 registry: Fix panic when server is unreachable  
    5c619ca1b website: Remove links to the getting started guide's old location  
    06275647e Update CHANGELOG.md  
    d5f9411f5 command: Fix bug when using terraform login on Windows  
    4b6d06cc5 Update CHANGELOG.md  
    dd01a3507 Update CHANGELOG.md  
    225466bc3 Cleanup after v0.12.23 release  

6. Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы).   
`>git log -S"func providerSource" --oneline`  
    функция func providerSource создана в commit 8c928e83589d90a031f811fae52a81be7153e82f  


7. Кто автор функции synchronizedWriters?  
`>git log -S"func synchronizedWriters" --pretty=format:"%h - %an %ae"`  
    >bdfea50cc - James Bardin j.bardin@gmail.com  
    5ac311e2a - Martin Atkins mart@degeneration.co.uk
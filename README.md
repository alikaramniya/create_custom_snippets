# create_custom_snippets

### توی این آموزش قصد دارم نحوه ساختن snippets های سفارشی توی ادیتور قدرتمند vim به شما دوستان آموزش بدم و در اخر هم میام و فایل کانفیگ خودم رو در اختیار شما قرار میدم

## Reference

### [ultisnips](https://github.com/SirVer/ultisnips)

### [Snippets in Vim](https://blog.prismatik.com.au/snippets-in-vim-43cf2ad79000)

### قدم اول

برای این که بتونیم snippet های سفارشی بسازیم باید اول از همه پلاگین های زیر رو نصب کنیم

```
Plug 'SirVer/ultisnips'
Plug 'honza/vim-snippets'
```

و برای coc هم باید دستور زیر رو بزنیم

```
:CocInstall coc-snippets
```

بعد میریم توی فایل .vimrc و کد های زیر رو داخلش قرار میدیم

```
let g:UltiSnipsExpandTrigger="<c-s>"
let g:UltiSnipsJumpForwardTrigger="<c-j>"
let g:UltiSnipsJumpBackwardTrigger="<c-k>"
```

الان برای اضافه کردن snippet جدید ما ابتدا میریم داخل محیط vim و بعد میریم توی مود کامند و دستور زیر رو اجرا میکنیم

```
:UltiSnipsEdit
```

بعد میریم به خط آخر و snippet خودمون رو اضافه میکنیم

```
snippet pub "function" b
${1:public} function ${2:functionName}(${3:arguements}) {
  $0
}
endsnippet
```

الان کافیه بریم توی محیط کد نویسی خودمون و از این snippet خودمون استفاده کنیم برای این کار pub رو مینویسیم و بعد ctrl-j (کنترل j) و بعد میبینیم که کد رو برای ما کامل میکنه

#### دقت کنید که فرمت snippet به جز pub که اسم snippet ما هست و کد هایی که بیت این دو تگ هستند بقیه قسمت ها باید به همون صورت باشن

با کنترل j و کنترل k میتونیم که بین قسمت های مختلف snippet خودمون جا به جا شیم

### زمانی که مینویسیم $0 این نقطه پایانی snippet ما هست

# chatbottele

Bot hoạt động
Cần token để có thể nhận cập nhật từ Telegram,  bằng cách gửi request đến URL này https://api.telegram.org/bot<token>/METHOD_NAME  với token đó. 
#Bắt đầu
tạo bot với BotFather ( là một bot )
##sử dụng phương thức getMe.
  https://api.telegram.org/bot<token>/getMe
// --> {"ok":true,"result":{"id":437852999,"is_bot":true,"first_name":"Reddit Bot","username":"SimpleReddit_Bot"}}
  Hiểu đoạn trên rằng mỗi khi cần cập nhật, sẽ gửi request đến URL đó bằng phương thức mong muốn
  Trong hướng dẫn này, chúng ta sẽ sử dụng Telegraf
 ## Bắt dầu code với NodeJS 
  Khởi tạo dự án và cài đặt Telegraf:
```jsx
npm init
npm install telegraf --save
```  
thêm nó vào script
```jsx  
const Telegraf = require('telegraf');
const app = new Telegraf(YOUR_TOKEN_HERE);
app.hears('hi', ctx => {
  return ctx.reply('Hey!');
});
app.startPolling();
 ```

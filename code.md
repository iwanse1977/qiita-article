⚠️ Please read the [VULNERABILITIES](VULNERABILITIES.md) document for a list of
fixed vulnerabilities
## 📦 Installation & Basic Usage

🔒 If you will be parsing untrusted input from users, please consider setting the `html_input` and `allow_unsafe_links` options per the example above. See <https://commonmark.thephpleague.com/security/> for more details. If you also do choose to allow raw HTML input from untrusted users, consider using a library (like [HTML Purifier](https://github.com/ezyang/htmlpurifier)) to provide additional HTML filtering.
## 📓 Documentation
## ⏫ Upgrading
## 💻 GitHub-Flavored Markdown
## 🗃️ Related Packages
## 🏷️ Versioning
## 🛠️ Maintenance & Support
## 👷‍♀️ Contributing
## 🧪 Testing
## 🚀 Performance Benchmarks
## 👥 Credits & Acknowledgements
## 📄 License
## 🏛️ Governance
## 🗺️ Who Uses It?
### 👨‍💻 Обо мне :
- На данный момент работаю в ООО "Команда Ф5" full-stack разработчиком 💻
### 📈 Моя статистика :
### 🛠️ Языки и инструменты разработки :



```sh
npm install blueimp-file-upload
```
```html
<script src="node_modules/blueimp-file-upload/js/jquery.fileupload.js"></script>
```
```js
$('#fileupload').fileupload();
```
  ```bash
    $ gem install rails
  ```

```php
use League\CommonMark\CommonMarkConverter;
$converter = new CommonMarkConverter([
    'html_input' => 'strip',
    'allow_unsafe_links' => false,
]);
echo $converter->convert('# Hello World!');
// <h1>Hello World!</h1>
```

<div align="center">
    <b>
        <a href="https://tidelift.com/subscription/pkg/packagist-league-commonmark?utm_source=packagist-league-commonmark&utm_medium=referral&utm_campaign=readme">Get professional support for league/commonmark with a Tidelift subscription</a>
    </b>
    <br>
    <sub>
        Tidelift helps make open source sustainable for maintainers while giving companies<br>assurances about security, maintenance, and licensing for their dependencies.
    </sub>
</div>

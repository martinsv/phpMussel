## Tài Liệu của phpMussel (Tiếng Việt).

### Nội dung
- 1. [LỜI GIỚI THIỆU](#SECTION1)
- 2A. [CẢCH ĐỂCÀI ĐẶT (CHO CÁC TRANG WEB CHỦ)](#SECTION2A)
- 2B. [CẢCH CÀI ĐẶT (CHO CLI)](#SECTION2B)
- 3A. [CÁCH SỬ DỤNG (CHO CÁC TRANG WEB CHỦ)](#SECTION3A)
- 3B. [CÁCH SỬ DỤNG (CHO CLI)](#SECTION3B)
- 4A. [LỆNH CHO BROWSER](#SECTION4A)
- 4B. [CLI (LỆNH CHO DÒNG GIAO DIỆN)](#SECTION4B)
- 5. [TÀI LIỆU BAO GỒM TRONG GÓI NÀY](#SECTION5)
- 6. [SỰ LỰA CHỌN CỦA CẤU HÌNH](#SECTION6)
- 7. [ĐỊNH DẠNG CỦA CHỬ KÝ](#SECTION7)
- 8. [NHỮNG VẤN ĐỀ HỢP TƯƠNG TÍCH](#SECTION8)

---


###1. <a name="SECTION1"></a>LỜI GIỚI THIỆU

Cảm ơn bạn đã chọn phpMussel, một loại bản PHP được thiết kế để phát hiện trojan, vi rút, phần mềm đọc hại và những gì có thể gây nguy hiểm trong những các tài liệu tài lên trên máy của bạn. Bất cứ nơi nào mà bản đã được nối, dưa trên chử ký của ClamAV và những người khác.

BẢN QUYỀN PHPMUSSEL 2013 và hơn GNU/GPLv2 by Caleb M (Maikuolan).

Bản này là chương trình miễn phí; bạn có thể phân phối lại hoạc sửa đổi dưới điều kiện của GNU Giấy Phép Công Cộng xuất bản bởi Free Software Foundation; một trong giấy phép phần hai, hoạc (tùy theo sự lựa chọn của bạn) bất kỳ phiên bản nào sau này. Bản này được phân phối với hy vọng rằng nó sẽ có hữu ích, nhưng mà KHÔNG CÓ BẢO HÀNH; ngay cả những bảo đảm ngụ ý KHẢ NĂNG BÁN HÀNG hoạc PHÙ HỢP VỚI MỤC ĐÍT VÀO. Hảy xem GNU Giấy Phép Công Cộng để biết them chi tiết, nằm trong hồ sơ `LICENSE` trong thư mục `_docs` của các gói liên quan và kho chứa của hồ sơ này có thể tiềm đước tại:
- <http://www.gnu.org/licenses/>.
- <http://opensource.org/licenses/>.

Chân thành cám ơn [ClamAV](http://www.clamav.net/) cho cả hai nguồn cảm hứng cho chương trình này và những chữ ký kịch bản này sử dụng, mà nếu không, bản này sẽ không có cơ hội tồn tại, hoặc ít nhất, sẽ có giá trị rất nhỏ.

Chân thành cám ơn Sourceforge và GitHub đã lưu trữ các tài liệu của chương trình này, và [Spambot Security](http://www.spambotsecurity.com/forum/viewforum.php?f=55) đã lưu trữ diễn đàn thảo luận của phpMussel, và các chữ ký sử dụng bởi phpMussel: [SecuriteInfo.com](http://www.securiteinfo.com/), [PhishTank](http://www.phishtank.com/), [NLNetLabs](http://nlnetlabs.nl/) vân vân, và chân thành cảm ơn những người đã ủng hộ chương trình này, và bất cứ ai khác mà tôi quên cảm ơn, và bạn, đã sử dụng bản này.

Tài liệu này và các gói liên quan của nó có thể được tải về miễn phí từ:
- [Sourceforge](http://phpmussel.sourceforge.net/).
- [GitHub](https://github.com/Maikuolan/phpMussel/).

---


###2A. <a name="SECTION2A"></a>CẢCH ĐỂCÀI ĐẶT (CHO CÁC TRANG WEB CHỦ)

Tôi hy vọng sẽ giản hóa quá trình này bằng cách thực hiện một cài đặt tại một thời điểm nào trong tương lai không quá xa, nhưng cho đến lúc đó, bạn hảy làm theo hướng dẫn để có thể cho phpMussel làm việc trên hầu hết các hệ thống và CMS:

1) Nếu bạn đang đọc cái này thì tôi hy vọng là bạn đã tải về một bản sao lưu trữ của bản, giải nén nội dung của nó và nó đang nằm ở một nơi nào đó trên máy tính của bạn. Từ đây, bạn sẽ muốn đặt nội dung ở một nơi trên máy chủ hoặc CMS của bạn. Một thư mục chẳng hạn như `/public_html/phpmussel/` hay tương tự (mặc dù sự lựa chọn của bạn không quan trọng, miễn là nó an toàn và bạn hài lòng với sự lựa chọn) sẽ đủ.. *Trước khi bạn bắt đầu tải lên, hảy tiếp tục đọc..*

2) Theo tùy chọn (khuyến khích những người dùng cao cấp, nhưng những người mới bắt đầu hoặc chưa có kinh nghiệm không nên chọn), hảy mở `phpmussel.ini` (nằm ớ trong `vault`) - Tài liệu này có chứa tất cả các chỉ thị sẵn cho phpMussel. Trên mỗi tùy chọn sẽ có chi tiết ngắn mô tả những gì nó làm. Hảy điều chỉnh các tùy chọn như bạn thấy phù hợp, theo bất cứ điều gì là thích hợp cho nhữn cài đặt của bạn. Lưu tập tin, đóng lại.

3) Tải nội dung lên (phpMussel và tài liệu của nó) vào thư mục bạn đã chọn trước (bạn không cần phải dùng hồ sơ `*.txt`/`*.md`, nhưng chủ yếu, bạn nên tải lên tất cả mọi thứ).

4) CMHOD cái `vault` thư mục thành "777". Các thư mục chính lưu trữ các nội dung (một trong những cái bạn đã chọn trước), bình thường, có thể riêng, nhưng tình hình CHMOD nên kiểm tra, nếu bạn đã có vấn đề cho phép trong quá khứ về hệ thống của bạn (theo mặc định, nên giống như "755").

5) Tiếp theo, bạn sẽ cần "nối" phpMussel vào hệ thống của bạn hoặc CMS. Có một số cách mà bạn có thể "nối" bản chẳng hạn như phpMussel vào hệ thống hoạc CMS, nhưng cách đơn giản nhất là cần có bản vào cốt lõi ở đầu của tài liệu hoạc hệ thống hoặc CMS của bạn (một mà thường sẽ luôn luôn được nạp khi ai đó truy cập bất kỳ trang nào trên trang web của bạn) bằng cách sử dụng một lời chỉ thị `require()` hoạc `include()`. Thường, cái nàu sẽ được lưu trong một thư mục như `/includes`, `/assets` hoạc `/functions`, và sẽ thường được gọi là `init.php`, `common_functions.php`, `functions.php` hoạc tương tự. Bạn sẽ cần tiềm ra hồ sơ nào cho trường hợp của bạn; Nếu bạn gặp khó khăn trong việc này, hãy truy cập diễn đàn hỗ trợ của phpMussel và cho chúng tôi biêt; Có thể là tôi họac các người dùng khác có có kinh nghiệm với các CMS mà bạn đang sử dụng (bạn phải biết mình đang sử dụng CMS nào), và như vậy, có thể cung cấp hỗ trợ trong trường hợp này. Để làm chuyện này [sử dụng `require()` họac `include()`], đánh các dòng mã sao đây vào đầu của cốt lõi của hồ sơ, thay thế các dây chứa bên trong các dấu ngoặc kép với địa chỉ chính xác của tài liệu `phpmussel.php` (địa chỉ địa phương, chứ không phải địa chỉ HTTP; nó sẽ nhình gióng địa chỉ kho nói ở trên).

`<?php require '/user_name/public_html/phpmussel/phpmussel.php'; ?>`

Lưu hồ sơ, đóng lại, tải lên lại.

-- CÁCH KHÁC --

Nếu bạn đang sử dụng trang chủ Apache và nếu bạn có thể truy cập `php.ini`, bạn có thể sử dụng `auto_prepend_file` chỉ thị để thêm vào trước phpMussel bất cứ khi nào bất kỳ yêu cầu PHP được xin. Gióng như:

`auto_prepend_file = "/user_name/public_html/phpmussel/phpmussel.php"`

Hoạc cái này trong hồ sơ `.htaccess`:

`php_value auto_prepend_file "/user_name/public_html/phpmussel/phpmussel.php"`

6) Tại điểm này, bạn đã xong! Nhưng mà, bạn nên kiểm tra nó ra để đảm bảo nó hoạt động đúng. Để kiểm tra các hồ sơ tải lên bảo vệ, thử tải lên các hồ sơ thử nghiệm bao gồm trong gói dưới `_testfiles` vào trang web của bạn thông qua các phương pháp tải lên dựa trên trình duyệt thông thường của bạn. Nếu tất cả mọi thứ đang hoạt động, một tin nhắn sẽ xuất hiện từ phpMussel xác nhận là việc tải lên đã bị chặn thành công. Nếu không có gì xuất hiện, đây là điều biểu hiện cho một vấn đề với sự hoạt động. Nếu bạn đang sử dụng chức năng cao cấp, hoặc sử dụng các loại chức năng quét khác có thể với công cụ này, bạn nên thử nó ra với những điều đó để đảm bảo nó hoạt động như yêu cầu.

---


###2B. <a name="SECTION2B"></a>CẢCH CÀI ĐẶT (CHO CLI)

Tôi hy vọng sẽ giản hóa quá trình này bằng cách thực hiện một cài đặt tại một thời điểm nào trong tương lai không quá xa, nhưng cho đến lúc đó, bạn hảy làm theo hướng dẫn để có thể cho phpMussel hoạt động với CLI (hảy cẩn thận, vào lúc này hỗ trợ cho CLI chỉ áp dụng với hệ thống dựa trên Windows; Linux và các hệ thống khác sẽ sau trong phiên bản sau này của phpMussel):

1) Nếu bạn đang đọc cái này thì tôi hy vọng là bạn đã tải về một bản sao lưu trữ của bản, giải nén nội dung của nó và nó đang nằm ở một nơi nào đó trên máy tính của bạn. Một khi bạn đã hài lòng với vị trí của phpMussel, hày tiếp tục.

2) phpMussel cần PHP được cài đặt trên máy chủ để thực hiện. Nếu bạn không có PHP cài trên máy, xin hảy cài php, theo hướng dẫn được cung cấp bởi người cài đặt php.

3) Theo tùy chọn (khuyến khích những người dùng cao cấp, nhưng những người mới bắt đầu hoặc chưa có kinh nghiệm không nên chọn), hảy mở `phpmussel.ini` (nằm ớ trong `vault`) - Tài liệu này có chứa tất cả các chỉ thị sẵn cho phpMussel. Trên mỗi tùy chọn sẽ có chi tiết ngắn mô tả những gì nó làm. Hảy điều chỉnh các tùy chọn như bạn thấy phù hợp, theo bất cứ điều gì là thích hợp cho nhữn cài đặt của bạn. Lưu tập tin, đóng lại.

4) Tùy ý, bạn có thể sử dụng phpMussel trong chế độ CLI dể hơn với cách tạo ra hồ sơ lô để tự động tải PHP và phpMussel. Để làm điều này, mở một chương trình văn bản đơn giản như Notepad hoạc Notepad++, đánh vào đường dẫn đầy đủ cho hồ sơ `php.exe` trong thư mục cài đặt PHP của bạn, tiếp theo là một khoảng trống, theo sau là đường dẫn đầy đủ đến hồ sơ `phpmussel.php` trong thư mục cài đặt phpMussel của bạn, lưu tài liệu với tư bổ sung ".bat" một nơi nào bạn sẽ tìm thấy dễ dàng, và nhấn đúp vào vào hồ sơ đó để chạy phpMussel trong tương lai.

5) Tại thời điểm này, bạ đã xong! Nhưng mà, bạn nên kiểm tra nó để đảm bảo sự hoạt động. Để kiểm tra phpMussel,chạy phpMussel và thử quét `_testfiles` thư mục cung cấp trong gói.

---


###3A. <a name="SECTION3A"></a>CÁCH SỬ DỤNG (CHO CÁC TRANG WEB CHỦ)

phpMussel is intended to be a script that'll function adequately right from the box with a bare minimum level of requirements on your part: Once it has been installed, basically, it simply should work.

Scanning of file uploads is automated and enabled by default, so nothing is required on your behalf for this particular function.

However, you're also able to instruct phpMussel to scan specific files, directories and/or archives. To do this, firstly, you'll need to ensure that the appropriate configuration is set in the `phpmussel.ini` file (`cleanup` must be disabled), and when done, in a PHP file that's hooked to phpMussel, use the following function in your code:

`phpMussel($what_to_scan,$output_type,$output_flatness);`

- `$what_to_scan` can be a string, an array, or an array of arrays, and indicates which file, files, directory and/or directories to scan.
- `$output_type` is a boolean, indicating the format for the scan results to be returned as. False instructs the function to return results as an integer (a returned result of -3 indicates problems were encountered with the phpMussel signatures files or signature map files and that they may possible be missing or corrupted, -2 indicates that corrupt data was detected during the scan and thus the scan failed to complete, -1 indicates that extensions or addons required by PHP to execute the scan were missing and thus the scan failed to complete, 0 indicates that the scan target doesn't exist and thus there was nothing to scan, 1 indicates that the target was successfully scanned and no problems were detected, and 2 indicates that the target was successfully scanned and problems were detected). True instructs the function to return results as human readable text. Additionally, in either case, the results can be accessed via global variables after scanning has completed. This variable is optional, defaulting to false.
- `$output_flatness` is a boolean, indicating to the function whether to return the results of scanning (when there are multiple scan targets) as an array or a string. False will return the results as an array. True will return the results as a string. This variable is optional, defaulting to false.

Examples:

```
 $results=phpMussel('/user_name/public_html/my_file.html',true,true);
 echo $results;
```

Returns something like this (as a string):

```
 Wed, 16 Sep 2013 02:49:46 +0000 Started.
 > Checking '/user_name/public_html/my_file.html':
 -> No problems found.
 Wed, 16 Sep 2013 02:49:47 +0000 Finished.
```

For a full break-down of what sort of signatures phpMussel uses during its scans and how it handles these signatures, refer to the Signature Format section of this README file.

If you encounter any false positives, if you encounter something new that you think should be blocked, or for anything else regarding signatures, please contact me about it so that I may make the necessary changes, which, if you do not contact me, I may not necessarily be aware of.

To disable signatures included with phpMussel (such as if you're experiencing a false positive specific to your purposes that shouldn't normally be removed from streamline), refer to the Greylisting notes within the Browser Commands section of this README file.

In addition to the default file upload scanning and the optional scanning of other files and/or directories specified via the above function, included in phpMussel is a function intended for scanning the body of email messages. This function behaves similarly to the standard phpMussel() function, but focuses solely on matching against the ClamAV email-based signatures. I have not tied these signatures into the standard phpMussel() function, because it is highly unlikely that you'd ever find the body of an incoming email message in need of scanning within a file upload targeted to a page where phpMussel is hooked, and thus, to tie these signatures into the phpMussel() function would be redundant. However, that said, having a separate function to match against these signatures could prove to be extremely useful for some, especially for those whose CMS or webfront system is somehow tied into their email system and for those parsing their emails via a PHP script that they could potentially hook into phpMussel. Configuration for this function, like all others, is controlled via the `phpmussel.ini` file. To use this function (you'll need to do your own implementation), in a PHP file that is hooked to phpMussel, use the following function in your code:

`phpMussel_mail($body);`

Where $body is body of the email message you wish to scan (additionally, you could try scanning new forum posts, inbound messages from your online contact form or similar). If any error occurs preventing the function from completing its scan, a value of -1 will be returned. If the function completes its scan and doesn't match anything, a value of 0 will be returned (meaning clean). If, however, the function does match something, a string will be returned containing a message declaring what it has matched.

In addition to the above, if you look at the source code, you may notice the function phpMusselD() and phpMusselR(). These functions are sub-functions of phpMussel(), and shouldn't be called directly outside of that parent function (not because of adverse effects, but rather, simply because it'd serve no purpose, and most probably won't actually work correctly anyhow).

There are many other controls and functions available within phpMussel for your use, too. For any such controls and functions which, by the end of this section of the README, have not yet been documented, please continue reading and refer to the Browser Commands section of this README file.

---


###3B. <a name="SECTION3B"></a>CÁCH SỬ DỤNG (CHO CLI)

Please refer to the "CẢCH CÀI ĐẶT (CHO CLI)" section of this readme file.

Be aware that, although future versions of phpMussel should support other systems, at this time, phpMussel CLI mode support is only optimized for use on Windows-based system (you can, of course, try it on other systems, but I can't guarantee it'll work as intended).

Also be aware that phpMussel is not the functional equivalent of a complete anti-virus suite, and unlike conventional anti-virus suites, doesn't monitor active memory or detect viruses on-the-fly! It'll only detect viruses contained by those specific files that you explicitly tell it to scan.

---


###4A. <a name="SECTION4A"></a>LỆNH CHO BROWSER

Once phpMussel has been installed and is correctly functioning on your system, if you've set the script_password and logs_password variables in your configuration file, you will be able to perform some limited number of administrative functions and input some number of commands to phpMussel via your browser. The reason these passwords need to be set in order to enable these browser-side controls is both to ensure proper security, proper protection of these browser-side controls and to ensure that there exists a way for these browser-side controls to be entirely disabled if they are not desired by you and/or other webmasters/administrators using phpMussel. So, in other words, to enable these controls, set a password, and to disable these controls, set no password. Alternatively, if you choose to enable these controls and then choose to disable these controls at a later date, there is a command to do this (such can be useful if you perform some actions that you feel could potentially compromise the delegated passwords and need to quickly disable these controls without modifying your configuration file).

A couple of reasons why you _**SHOULD**_ enable these controls:
- Provides a way to greylist signatures on-the-fly in instances such as when you discover a signature that is producing a false-positive while uploading files to your system and you don't have time to manually edit and reupload your greylist file.
- Provides a way for you to allow someone other than yourself to control your copy of phpMussel without the implicit need to grant them access to FTP.
- Provides a way to provide controlled access to your log files.
- Provides an easy way to update phpMussel when updates are available.
- Provides a way for you to monitor phpMussel when FTP access or other conventional access points for monitoring phpMussel are not available.

A couple of reasons why you should _**NOT**_ enable these controls:
- Provides a vector for potential attackers and undesirables to determine whether you're using phpMussel or not (although, this could be both a reason for and a reason against, depending on perspective) by way of blindly sending commands to servers as a means to probe. On one hand, this could discourage attackers from targeting your system if they learn that you're using phpMussel, assuming that they are probing because their attack method is rendered ineffective as a result of using phpMussel. However, on the other hand, if some unforeseen and currently unknown exploit within phpMussel or a future version thereof comes to light, and if it could potentially provide an attack vector, a positive result from such probing could actually encourage attackers to target your system.
- If your delegated passwords were ever compromised, unless changed, could provide a way for an attacker to bypass whatever signatures may be otherwise normally preventing their attacks from succeeding, or even potentially disable phpMussel altogether, thus providing a way to render the effectiveness of phpMussel moot.

Either way, regardless of what you choose, the choice is ultimately yours. By default, these controls will be disabled, but have a think about it, and if you decide you want them, this section explains both how to enable them and how to use them.

A list of available browser-side commands:

scan_log
- Password required: logs_password
- Other requirements: scan_log must be set.
- Required parameters: (none)
- Optional parameters: (none)
- Example: `?logspword=[logs_password]&phpmussel=scan_log`
- What it does: Prints the contents of your scan_log file to the screen.

scan_kills
- Password required: logs_password
- Other requirements: scan_kills must be set.
- Required parameters: (none)
- Optional parameters: (none)
- Example: `?logspword=[logs_password]&phpmussel=scan_kills`
- What it does: Prints the contents of your scan_kills file to the screen.

controls_lockout
- Password required: logs_password OR script_password
- Other requirements: (none)
- Required parameters: (none)
- Optional parameters: (none)
- Example 1: `?logspword=[logs_password]&phpmussel=controls_lockout`
- Example 2: `?pword=[script_password]&phpmussel=controls_lockout`
- What it does: Disables ("locks out") all browser-side controls. This should be used if you suspect that either of your passwords have been compromised (this can happen if you're using these controls from a computer that's not secured and/or not trusted). controls_lockout works by creating a file, `controls.lck`, in your vault, that phpMussel will check for before performing any commands of any kind. Once this happens, to reenable controls, you'll need to manually delete the `controls.lck` file via FTP or similar. Can be called using either password.

disable
- Password required: script_password
- Other requirements: (none)
- Required parameters: (none)
- Optional parameters: (none)
- Example: `?pword=[script_password]&phpmussel=disable`
- What it does: Disables phpMussel. This should be used if you're performing any updates or changes to your system or if you're installing any new software or modules to your system that either does or potentially could trigger false positives. This should also be used if you're having any problems with phpMussel but don't wish to remove it from your system. Once this happens, to reenable phpMussel, use "enable".

enable
- Password required: script_password
- Other requirements: (none)
- Required parameters: (none)
- Optional parameters: (none)
- Example: `?pword=[script_password]&phpmussel=enable`
- What it does: Enables phpMussel. This should be used if you've previously disabled phpMussel using "disable" and want to reenable it.

update
- Password required: script_password
- Other requirements: `update.dat` and `update.inc` must exist.
- Required parameters: (none)
- Optional parameters: (none)
- Example: `?pword=[script_password]&phpmussel=update`
- What it does: Checks for updates to both phpMussel and its signatures. If update checks succeed and updates are found, will attempt to download and install these updates. If update checks fail, update will abort. Results of the entire process are printed to the screen. I recommend checking at least once per month to ensure that your signatures and your copy of phpMussel are kept up to-date (unless, of course, you're checking for updates and installing them manually, which, I'd still recommend doing at least once per month). Checking more than twice per month is probably pointless, considering that I'm very unlikely to be able to produce updates of any kind more frequently than that (nor do I particularly want to for the most part).

greylist
- Password required: script_password
- Other requirements: (none)
- Required parameters: [Name of signature to be greylisted]
- Optional parameters: (none)
- Example: `?pword=[script_password]&phpmussel=greylist&musselvar=[Signature]`
- What it does: Add a signature to the greylist.

greylist_clear
- Password required: script_password
- Other requirements: (none)
- Required parameters: (none)
- Optional parameters: (none)
- Example: `?pword=[script_password]&phpmussel=greylist_clear`
- What it does: Clears the entire greylist.

greylist_show
- Password required: script_password
- Other requirements: (none)
- Required parameters: (none)
- Optional parameters: (none)
- Example: `?pword=[script_password]&phpmussel=greylist_show`
- What it does: Prints the contents of the greylist to the screen.

---


###4B. <a name="SECTION4B"></a>CLI (LỆNH CHO DÒNG GIAO DIỆN)

phpMussel can be run as an interactive file scanner in CLI mode under Windows-based systems. Refer to the "CẢCH CÀI ĐẶT (CHO CLI)" section of this readme file for more details.

For a list of available CLI commands, at the CLI prompt, type 'c', and press Enter.

---


###5. <a name="SECTION5"></a>TÀI LIỆU BAO GỒM TRONG GÓI NÀY

The following is a list of all of the files that should have been included in the archived copy of this script when you downloaded it, any files that may be potentially created as a result of your using this script, along with a short description of what all these files are for.

Hồ sơ                                      | Chi tiết
-------------------------------------------|--------------------------------------
/phpmussel.php                             | Hồ sơ tải. Tải bản chính, tải lên, vân vân. Đây là điều bạn cần nối vào (cần thiết)!
/web.config                                | Một hồ sơ cấu hình của ASP.NET (trong trường hợp này, để bảo vệ `/vault` thư mực khỏi bị truy cập bởi những nguồn không có quền trong trường hợp bản được cài trên serever chạy trên công nghệ ASP.NET).
/_docs/                                    | Thư mực tài liệu (Chứa nhiều loại hồ sơ).
/_docs/change_log.txt                      | Kỷ lục của những sự thay đổi được thực hiện cho các kịch bản khác nhau giữa các phiên bản (không cần thiết cho chức năng phù hợp của kịch bản).
/_docs/readme.de.md                        | Tài liệu: DEUTSCH
/_docs/readme.de.txt                       | Tài liệu: DEUTSCH
/_docs/readme.en.md                        | Tài liệu: ENGLISH
/_docs/readme.en.txt                       | Tài liệu: ENGLISH
/_docs/readme.es.md                        | Tài liệu: ESPAÑOL
/_docs/readme.es.txt                       | Tài liệu: ESPAÑOL
/_docs/readme.fr.md                        | Tài liệu: FRANÇAIS
/_docs/readme.fr.txt                       | Tài liệu: FRANÇAIS
/_docs/readme.id.md                        | Tài liệu: BAHASA INDONESIA
/_docs/readme.id.txt                       | Tài liệu: BAHASA INDONESIA
/_docs/readme.it.md                        | Tài liệu: ITALIANO
/_docs/readme.it.txt                       | Tài liệu: ITALIANO
/_docs/readme.nl.md                        | Tài liệu: NEDERLANDSE
/_docs/readme.nl.txt                       | Tài liệu: NEDERLANDSE
/_docs/readme.pt.md                        | Tài liệu: PORTUGUÊS
/_docs/readme.pt.txt                       | Tài liệu: PORTUGUÊS
/_docs/readme.ru.md                        | Tài liệu: РУССКИЙ
/_docs/readme.ru.txt                       | Tài liệu: РУССКИЙ
/_docs/signatures_tally.txt                | Lý lịch của net-shift có bao gồm chữ ký (không cần thiết cho chức năng phù hợp của kịch bản).
/_testfiles/                               | Kiểm tra tập tin thư mục (chứa các tập tin khác nhau). Tất cả các hồ sơ chứa những hồ sơ thử nghiệm để thử nghiệm nếu phpMussel đã được cài đặt đúng trên hệ thống của bạn, và bạn không cần phải tải lên thư mục này hoặc bất kỳ các hồ sơ của mình trừ khi làm xét nghiệm như vậy.
/_testfiles/ascii_standard_testfile.txt    | Kiểm tra hồ sơ cho xét nghiệm phpMussel chữ ký ASCII bình thường.
/_testfiles/coex_testfile.rtf              | Kiểm tra hồ sơ cho xét nghiệm phpMussel chử ký kéo dài phức tạp.
/_testfiles/exe_standard_testfile.exe      | Test file for testing phpMussel PE signatures.
/_testfiles/general_standard_testfile.txt  | Test file for testing phpMussel general signatures.
/_testfiles/graphics_standard_testfile.gif | Test file for testing phpMussel graphics signatures.
/_testfiles/html_standard_testfile.txt     | Test file for testing phpMussel normalised HTML signatures.
/_testfiles/md5_testfile.txt               | Test file for testing phpMussel MD5 signatures.
/_testfiles/metadata_testfile.tar          | Test file for testing phpMussel metadata signatures and for testing TAR file support on your system.
/_testfiles/metadata_testfile.txt.gz       | Test file for testing phpMussel metadata signatures and for testing GZ file support on your system.
/_testfiles/metadata_testfile.zip          | Test file for testing phpMussel metadata signatures and for testing ZIP file support on your system.
/_testfiles/ole_testfile.ole               | Test file for testing phpMussel OLE signatures.
/_testfiles/pdf_standard_testfile.pdf      | Test file for testing phpMussel PDF signatures.
/_testfiles/pe_sectional_testfile.exe      | Test file for testing phpMussel PE Sectional signatures.
/_testfiles/swf_standard_testfile.swf      | Test file for testing phpMussel SWF signatures.
/_testfiles/xdp_standard_testfile.xdp      | Test file for testing phpMussel XML/XDP-Chunk signatures.
/vault/                                    | Vault directory (contains various files).
/vault/cache/                              | Cache directory (for temporary data).
/vault/cache/.htaccess                     | A hypertext access file (in this instance, to protect sensitive files belonging to the script from being accessed by non-authorised sources).
/vault/lang/                               | Contains phpMussel language data.
/vault/lang/.htaccess                      | A hypertext access file (in this instance, to protect sensitive files belonging to the script from being accessed by non-authorised sources).
/vault/lang/lang.de.inc                    | Language data: DEUTSCH
/vault/lang/lang.en.inc                    | Language data: ENGLISH
/vault/lang/lang.es.inc                    | Language data: ESPAÑOL
/vault/lang/lang.fr.inc                    | Language data: FRANÇAIS
/vault/lang/lang.id.inc                    | Language data: BAHASA INDONESIA
/vault/lang/lang.it.inc                    | Language data: ITALIANO
/vault/lang/lang.ja.inc                    | Language data: 日本語
/vault/lang/lang.nl.inc                    | Language data: NEDERLANDSE
/vault/lang/lang.pt.inc                    | Language data: PORTUGUÊS
/vault/lang/lang.ru.inc                    | Language data: РУССКИЙ
/vault/lang/lang.vi.inc                    | Language data: TIẾNG VIỆT
/vault/lang/lang.zh.inc                    | Language data: 中文（简体）
/vault/lang/lang.zh-TW.inc                 | Language data: 中文（傳統）
/vault/quarantine/                         | Quarantine directory (contains quarantined files).
/vault/quarantine/.htaccess                | A hypertext access file (in this instance, to protect sensitive files belonging to the script from being accessed by non-authorised sources).
/vault/.htaccess                           | A hypertext access file (in this instance, to protect sensitive files belonging to the script from being accessed by non-authorised sources).
/vault/ascii_clamav_regex.cvd              | File for normalised ASCII signatures.
/vault/ascii_clamav_regex.map              | File for normalised ASCII signatures.
/vault/ascii_clamav_standard.cvd           | File for normalised ASCII signatures.
/vault/ascii_clamav_standard.map           | File for normalised ASCII signatures.
/vault/ascii_custom_regex.cvd              | File for normalised ASCII signatures.
/vault/ascii_custom_standard.cvd           | File for normalised ASCII signatures.
/vault/ascii_mussel_regex.cvd              | File for normalised ASCII signatures.
/vault/ascii_mussel_standard.cvd           | File for normalised ASCII signatures.
/vault/coex_clamav.cvd                     | File for complex extended signatures.
/vault/coex_custom.cvd                     | File for complex extended signatures.
/vault/coex_mussel.cvd                     | File for complex extended signatures.
/vault/elf_clamav_regex.cvd                | File for ELF signatures.
/vault/elf_clamav_regex.map                | File for ELF signatures.
/vault/elf_clamav_standard.cvd             | File for ELF signatures.
/vault/elf_clamav_standard.map             | File for ELF signatures.
/vault/elf_custom_regex.cvd                | File for ELF signatures.
/vault/elf_custom_standard.cvd             | File for ELF signatures.
/vault/elf_mussel_regex.cvd                | File for ELF signatures.
/vault/elf_mussel_standard.cvd             | File for ELF signatures.
/vault/exe_clamav_regex.cvd                | File for PE (Portable Executable) signatures.
/vault/exe_clamav_regex.map                | File for PE (Portable Executable) signatures.
/vault/exe_clamav_standard.cvd             | File for PE (Portable Executable) signatures.
/vault/exe_clamav_standard.map             | File for PE (Portable Executable) signatures.
/vault/exe_custom_regex.cvd                | File for PE (Portable Executable) signatures.
/vault/exe_custom_standard.cvd             | File for PE (Portable Executable) signatures.
/vault/exe_mussel_regex.cvd                | File for PE (Portable Executable) signatures.
/vault/exe_mussel_standard.cvd             | File for PE (Portable Executable) signatures.
/vault/filenames_clamav.cvd                | File for filename signatures.
/vault/filenames_custom.cvd                | File for filename signatures.
/vault/filenames_mussel.cvd                | File for filename signatures.
/vault/general_clamav_regex.cvd            | File for general signatures.
/vault/general_clamav_regex.map            | File for general signatures.
/vault/general_clamav_standard.cvd         | File for general signatures.
/vault/general_clamav_standard.map         | File for general signatures.
/vault/general_custom_regex.cvd            | File for general signatures.
/vault/general_custom_standard.cvd         | File for general signatures.
/vault/general_mussel_regex.cvd            | File for general signatures.
/vault/general_mussel_standard.cvd         | File for general signatures.
/vault/graphics_clamav_regex.cvd           | File for graphics signatures.
/vault/graphics_clamav_regex.map           | File for graphics signatures.
/vault/graphics_clamav_standard.cvd        | File for graphics signatures.
/vault/graphics_clamav_standard.map        | File for graphics signatures.
/vault/graphics_custom_regex.cvd           | File for graphics signatures.
/vault/graphics_custom_standard.cvd        | File for graphics signatures.
/vault/graphics_mussel_regex.cvd           | File for graphics signatures.
/vault/graphics_mussel_standard.cvd        | File for graphics signatures.
/vault/greylist.csv                        | CSV of greylisted signatures indicating to phpMussel which signatures it should be ignoring (file automatically recreated if deleted).
/vault/hex_general_commands.csv            | Hex-encoded CSV of general command detections optionally used by phpMussel.
/vault/html_clamav_regex.cvd               | File for normalised HTML signatures.
/vault/html_clamav_regex.map               | File for normalised HTML signatures.
/vault/html_clamav_standard.cvd            | File for normalised HTML signatures.
/vault/html_clamav_standard.map            | File for normalised HTML signatures.
/vault/html_custom_regex.cvd               | File for normalised HTML signatures.
/vault/html_custom_standard.cvd            | File for normalised HTML signatures.
/vault/html_mussel_regex.cvd               | File for normalised HTML signatures.
/vault/html_mussel_standard.cvd            | File for normalised HTML signatures.
/vault/lang.inc                            | Language data.
/vault/macho_clamav_regex.cvd              | File for Mach-O signatures.
/vault/macho_clamav_regex.map              | File for Mach-O signatures.
/vault/macho_clamav_standard.cvd           | File for Mach-O signatures.
/vault/macho_clamav_standard.map           | File for Mach-O signatures.
/vault/macho_custom_regex.cvd              | File for Mach-O signatures.
/vault/macho_custom_standard.cvd           | File for Mach-O signatures.
/vault/macho_mussel_regex.cvd              | File for Mach-O signatures.
/vault/macho_mussel_standard.cvd           | File for Mach-O signatures.
/vault/mail_clamav_regex.cvd               | File for mail signatures.
/vault/mail_clamav_regex.map               | File for mail signatures.
/vault/mail_clamav_standard.cvd            | File for mail signatures.
/vault/mail_clamav_standard.map            | File for mail signatures.
/vault/mail_custom_regex.cvd               | File for mail signatures.
/vault/mail_custom_standard.cvd            | File for mail signatures.
/vault/mail_mussel_regex.cvd               | File for mail signatures.
/vault/mail_mussel_standard.cvd            | File for mail signatures.
/vault/mail_mussel_standard.map            | File for mail signatures.
/vault/md5_clamav.cvd                      | File for MD5 based signatures.
/vault/md5_custom.cvd                      | File for MD5 based signatures.
/vault/md5_mussel.cvd                      | File for MD5 based signatures.
/vault/metadata_clamav.cvd                 | File for archive metadata signatures.
/vault/metadata_custom.cvd                 | File for archive metadata signatures.
/vault/metadata_mussel.cvd                 | File for archive metadata signatures.
/vault/ole_clamav_regex.cvd                | File for OLE signatures.
/vault/ole_clamav_regex.map                | File for OLE signatures.
/vault/ole_clamav_standard.cvd             | File for OLE signatures.
/vault/ole_clamav_standard.map             | File for OLE signatures.
/vault/ole_custom_regex.cvd                | File for OLE signatures.
/vault/ole_custom_standard.cvd             | File for OLE signatures.
/vault/ole_mussel_regex.cvd                | File for OLE signatures.
/vault/ole_mussel_standard.cvd             | File for OLE signatures.
/vault/pdf_clamav_regex.cvd                | File for PDF signatures.
/vault/pdf_clamav_regex.map                | File for PDF signatures.
/vault/pdf_clamav_standard.cvd             | File for PDF signatures.
/vault/pdf_clamav_standard.map             | File for PDF signatures.
/vault/pdf_custom_regex.cvd                | File for PDF signatures.
/vault/pdf_custom_standard.cvd             | File for PDF signatures.
/vault/pdf_mussel_regex.cvd                | File for PDF signatures.
/vault/pdf_mussel_standard.cvd             | File for PDF signatures.
/vault/pe_clamav.cvd                       | File for PE Sectional signatures.
/vault/pe_custom.cvd                       | File for PE Sectional signatures.
/vault/pe_mussel.cvd                       | File for PE Sectional signatures.
/vault/pex_custom.cvd                      | File for PE extended signatures.
/vault/pex_mussel.cvd                      | File for PE extended signatures.
/vault/phpmussel.inc                       | Core Script; The main body and guts of phpMussel (essential)!
/vault/phpmussel.ini                       | Configuration file; Contains all the configuration options of phpMussel, telling it what to do and how to operate correctly (essential)!
※ /vault/scan_log.txt                     | A record of everything scanned by phpMussel.
※ /vault/scan_kills.txt                   | A record of every file upload blocked/killed by phpMussel.
/vault/swf_clamav_regex.cvd                | File for the Shockwave signatures.
/vault/swf_clamav_regex.map                | File for the Shockwave signatures.
/vault/swf_clamav_standard.cvd             | File for the Shockwave signatures.
/vault/swf_clamav_standard.map             | File for the Shockwave signatures.
/vault/swf_custom_regex.cvd                | File for the Shockwave signatures.
/vault/swf_custom_standard.cvd             | File for the Shockwave signatures.
/vault/swf_mussel_regex.cvd                | File for the Shockwave signatures.
/vault/swf_mussel_standard.cvd             | File for the Shockwave signatures.
/vault/switch.dat                          | Controls and sets certain variables.
/vault/template.html                       | Template file; Template for HTML output produced by phpMussel for its blocked file upload message (the message seen by the uploader).
/vault/template_custom.html                | Template file; Template for HTML output produced by phpMussel for its blocked file upload message (the message seen by the uploader).
/vault/update.dat                          | File containing version information for both the phpMussel script and the phpMussel signatures. If you ever want to automatically update phpMussel or want to update phpMussel via your browser, this file is essential.
/vault/update.inc                          | Update Script; Required for automatic updates and for updating phpMussel via your browser, but not required otherwise.
/vault/whitelist_clamav.cvd                | Hồ sơ riêng cho danh sách trắng.
/vault/whitelist_custom.cvd                | Hồ sơ riêng cho danh sách trắng.
/vault/whitelist_mussel.cvd                | Hồ sơ riêng cho danh sách trắng.
/vault/xmlxdp_clamav_regex.cvd             | Hồ sơ cho chữ ký XML/XDP-Chunk.
/vault/xmlxdp_clamav_regex.map             | Hồ sơ cho chữ ký XML/XDP-Chunk.
/vault/xmlxdp_clamav_standard.cvd          | Hồ sơ cho chữ ký XML/XDP-Chunk.
/vault/xmlxdp_clamav_standard.map          | Hồ sơ cho chữ ký XML/XDP-Chunk.
/vault/xmlxdp_custom_regex.cvd             | Hồ sơ cho chữ ký XML/XDP-Chunk.
/vault/xmlxdp_custom_standard.cvd          | Hồ sơ cho chữ ký XML/XDP-Chunk.
/vault/xmlxdp_mussel_regex.cvd             | Hồ sơ cho chữ ký XML/XDP-Chunk.
/vault/xmlxdp_mussel_standard.cvd          | Hồ sơ cho chữ ký XML/XDP-Chunk.

※ Tên tài liệu có thể thay đổi tuy theo các quy định của cấu hình (in `phpmussel.ini`).

####*REGARDING SIGNATURE FILES*
CVD is an acronym for "ClamAV Virus Definitions", in reference both to how ClamAV refers to its own signatures and to the use of those signatures for phpMussel; Files ending with "CVD" contain signatures.

Files ending with "MAP", quite literally, map which signatures phpMussel should and shouldn't use for individual scans; Not all signatures are necessarily required for every single scan, so, phpMussel uses maps of the signature files to speed up the scanning process (a process that would otherwise be extremely slow and tedious).

Signature files marked with "_regex" contain signatures that utilise regular expression pattern checking (regex).

Signature files marked with "_standard" contain signatures that specifically don't utilise any form of pattern checking.

Signature files marked with neither "_regex" nor "_standard" will be as one or the other, but not both (refer to the Signature Format section of this README file for documentation and specific details).

Signature files marked with "_clamav" contain signatures that are sourced entirely from the ClamAV database (GNU/GPL).

Signature files marked with "_custom", by default, don't contain any signatures at all; These such files exist to give you somewhere to place your own custom signatures, if you come up with any of your own.

Signature files marked with "_mussel" contain signatures that specifically are not sourced from ClamAV, signatures which, generally, I've either come up with myself and/or based on information gathered from various sources.


---


###6. <a name="SECTION6"></a>SỰ LỰA CHỌN CỦA CẤU HÌNH
The following is a list of variables found in the `phpmussel.ini` configuration file of phpMussel, along with a description of their purpose and function.

####"general" (Category)
General phpMussel configuration.

"script_password"
- As a convenience, phpMussel will allow certain functions (including the ability to update phpMussel on-the-fly) to be manually triggered via POST, GET and QUERY. However, as a security precaution, to do this, phpMussel will expect a password to be included with the command, as to ensure that it's you, and not someone else, attempting to manually trigger these functions. Set script_password to whatever password you would like to use. If no password is set, manual triggering will be disabled by default. Use something you will remember but which is hard for others to guess.
- Has no influence in CLI mode.

"logs_password"
- The same as script_password, but for viewing the contents of scan_log and scan_kills. Having separate passwords can be useful if you want to give someone else access to one set of functions but not the other.
- Has no influence in CLI mode.

"cleanup"
- Unset variables and cache used by the script after the initial upload scanning? False = No, True = Yes [Default]. If you -aren't- using the script beyond the initial scanning of uploads, you should set this to `true` (yes), to minimize memory usage. If you -are- using the script beyond the initial scanning of uploads, should set to `false` (no), to avoid unnecessarily reloading duplicate data into memory. In general practice, it should usually be set to `true`, but, if you do this, you won't be able to use the script for anything other than the initial file upload scanning.
- Has no influence in CLI mode.

"scan_log"
- Filename of file to log all scanning results to. Specify a filename, or leave blank to disable.

"scan_kills"
- Filename of file to log all records of blocked or killed uploads to. Specify a filename, or leave blank to disable.

"ipaddr"
- Where to find IP address of connecting request? (Useful for services such as Cloudflare and the likes) Default = REMOTE_ADDR. WARNING: Don't change this unless you know what you're doing!

"forbid_on_block"
- Should phpMussel send 403 headers with the file upload blocked message, or stick with the usual 200 OK? 0 = No (200) [Default], 1 = Yes (403).

"delete_on_sight"
- Enabling this directive will instruct the script to attempt to immediately delete any scanned attempted file upload matching any detection criteria, whether via signatures or otherwise. Files determined to be "clean" won't be touched. In the case of archives, the entire archive will be deleted, regardless of whether or not the offending file is only one of several files contained within the archive. For the case of file upload scanning, usually, it isn't necessary to enable this directive, because usually, PHP will automatically purge the contents of its cache when execution has finished, meaning it'll usually delete any files uploaded through it to the server unless they've been moved, copied or deleted already. This directive is added here as an extra measure of security for those whose copies of PHP mightn't always behave in the manner expected. False = After scanning, leave the file alone [Default], True = After scanning, if not clean, delete immediately.

"lang"
- Specify the default language for phpMussel.

"lang_override"
- Specify if phpMussel should, when possible, override the language specification with the language preference declared by inbound requests (HTTP_ACCEPT_LANGUAGE). 0 - No [Default], 1 - Yes.

"lang_acceptable"
- The `lang_acceptable` directive tells phpMussel which languages may be accepted by the script from `lang` or from `HTTP_ACCEPT_LANGUAGE`. This directive should **ONLY** be modified if you're adding your own customised language files or forcibly removing language files. The directive is a comma delimited string of the codes used by those languages accepted by the script.

"quarantine_key"
- phpMussel is able to quarantine flagged attempted file uploads in isolation within the phpMussel vault, if this is something you want it to do. Casual users of phpMussel that simply wish to protect their websites or hosting environment without having any interest in deeply analysing any flagged attempted file uploads should leave this functionality disabled, but any users interested in further analysis of flagged attempted file uploads for malware research or for similar such things should enable this functionality. Quarantining of flagged attempted file uploads can sometimes also assist in debugging false-positives, if this is something that frequently occurs for you. To disable quarantine functionality, simply leave the `quarantine_key` directive empty, or erase the contents of that directive if it isn't already empty. To enable quarantine functionality, enter some value into the directive. The `quarantine_key` is an important security feature of the quarantine functionality required as a means of preventing the quarantine functionality from being exploited by potential attackers and as a means of preventing any potential execution of data stored within the quarantine. The `quarantine_key` should be treated in the same manner as your passwords: The longer the better, and guard it tightly. For best effect, use in conjunction with `delete_on_sight`.

"quarantine_max_filesize"
- The maximum allowable filesize of files to be quarantined. Files larger than the value specified will NOT be quarantined. This directive is important as a means of making it more difficult for any potential attackers to flood your quarantine with unwanted data potentially causing run-away data usage on your hosting service. Value is in KB. Default =2048 =2048KB =2MB.

"quarantine_max_usage"
- The maximum memory usage allowed for the quarantine. If the total memory used by the quarantine reaches this value, the oldest quarantined files will be deleted until the total memory used no longer reaches this value. This directive is important as a means of making it more difficult for any potential attackers to flood your quarantine with unwanted data potentially causing run-away data usage on your hosting service. Value is in KB. Default =65536 =65536KB =64MB.

"honeypot_mode"
- When honeypot mode is enabled, phpMussel will attempt to quarantine every single file upload that it encounters, regardless of whether or not the file being uploaded matches any included signatures, and no actual scanning or analysis of those attempted file uploads will actually occur. This functionality should be useful for those that wish to use phpMussel for the purposes of virus/malware research, but it's neither recommended to enable this functionality if the intended use of phpMussel by the user is for actual file upload scanning, nor recommended to use the honeypot functionality for purposes other than honeypotting. By default, this option is disabled. 0 = Disabled [Default], 1 = Enabled.

"scan_cache_expiry"
- For how long should phpMussel cache the results of scanning? Value is the number of seconds to cache the results of scanning for. Default is 21600 seconds (6 hours); A value of 0 will disable caching the results of scanning.

"disable_cli"
- Disable CLI mode? CLI mode is enabled by default, but can sometimes interfere with certain testing tools (such as PHPUnit, for example) and other CLI-based applications. If you don't need to disable CLI mode, you should ignore this directive. 0 = Enable CLI mode [Default], 1 = Disable CLI mode.

####"signatures" (Category)
Signatures configuration.
- %%%_clamav = ClamAV signatures (both mains and daily).
- %%%_custom = Your custom signatures (if you've written any).
- %%%_mussel = phpMussel signatures included in your current signatures set that aren't from ClamAV.

Check against MD5 signatures when scanning? False = No, True = Yes [Default].
- "md5_clamav"
- "md5_custom"
- "md5_mussel"

Check against general signatures when scanning? False = No, True = Yes [Default].
- "general_clamav"
- "general_custom"
- "general_mussel"

Check against normalised ASCII signatures when scanning? False = No, True = Yes [Default].
- "ascii_clamav"
- "ascii_custom"
- "ascii_mussel"

Check against normalised HTML signatures when scanning? False = No, True = Yes [Default].
- "html_clamav"
- "html_custom"
- "html_mussel"

Check PE (Portable Executable) files (EXE, DLL, etc) against PE Sectional signatures when scanning? False = No, True = Yes [Default].
- "pe_clamav"
- "pe_custom"
- "pe_mussel"

Check PE (Portable Executable) files (EXE, DLL, etc) against PE extended signatures when scanning? False = No, True = Yes [Default].
- "pex_custom"
- "pex_mussel"

Check PE (Portable Executable) files (EXE, DLL, etc) against PE signatures when scanning? False = No, True = Yes [Default].
- "exe_clamav"
- "exe_custom"
- "exe_mussel"

Check ELF files against ELF signatures when scanning? False = No, True = Yes [Default].
- "elf_clamav"
- "elf_custom"
- "elf_mussel"

Check Mach-O files (OSX, etc) against Mach-O signatures when scanning? False = No, True = Yes [Default].
- "macho_clamav"
- "macho_custom"
- "macho_mussel"

Check graphics files against graphics based signatures when scanning? False = No, True = Yes [Default].
- "graphics_clamav"
- "graphics_custom"
- "graphics_mussel"

Check archive contents against archive metadata signatures when scanning? False = No, True = Yes [Default].
- "metadata_clamav"
- "metadata_custom"
- "metadata_mussel"

Check OLE objects against OLE signatures when scanning? False = No, True = Yes [Default].
- "ole_clamav"
- "ole_custom"
- "ole_mussel"

Check filenames against filename based signatures when scanning? False = No, True = Yes [Default].
- "filenames_clamav"
- "filenames_custom"
- "filenames_mussel"

Allow scanning with phpMussel_mail()? False = No, True = Yes [Default].
- "mail_clamav"
- "mail_custom"
- "mail_mussel"

Enable file specific whitelist? False = No, True = Yes [Default].
- "whitelist_clamav"
- "whitelist_custom"
- "whitelist_mussel"

Check XML/XDP chunks against XML/XDP-chunk signatures when scanning? False = No, True = Yes [Default].
- "xmlxdp_clamav"
- "xmlxdp_custom"
- "xmlxdp_mussel"

Check against complex extended signatures when scanning? False = No, True = Yes [Default].
- "coex_clamav"
- "coex_custom"
- "coex_mussel"

Check against PDF signatures when scanning? False = No, True = Yes [Default].
- "pdf_clamav"
- "pdf_custom"
- "pdf_mussel"

Check against Shockwave signatures when scanning? False = No, True = Yes [Default].
- "swf_clamav"
- "swf_custom"
- "swf_mussel"

Signature matching length limiting options. Only change these if you know what you're doing. SD = Standard signatures. RX = PCRE (Perl Compatible Regular Expressions, or "Regex") signatures. FN = Filename signatures. If you notice PHP crashing when phpMussel attempts to scan, try lowering these "max" values. If possible and convenient, let me know when this happens and the results of whatever you try.
- "fn_siglen_min"
- "fn_siglen_max"
- "rx_siglen_min"
- "rx_siglen_max"
- "sd_siglen_min"
- "sd_siglen_max"

"fail_silently"
- Should phpMussel report when signatures files are missing or corrupted? If fail_silently is disabled, missing and corrupted files will be reported on scanning, and if fail_silently is enabled, missing and corrupted files will be ignored, with scanning reporting for those files that there aren't any problems. This should generally be left alone unless you're experiencing crashes or similar problems. 0 = Disabled, 1 = Enabled [Default].

"fail_extensions_silently"
- Should phpMussel report when extensions are missing? If fail_extensions_silently is disabled, missing extensions will be reported on scanning, and if fail_extensions_silently is enabled, missing extensions will be ignored, with scanning reporting for those files that there aren't any problems. Disabling this directive may potentially increase your security, but may also lead to an increase of false positives. 0 = Disabled, 1 = Enabled [Default].

"detect_adware"
- Should phpMussel parse signatures for detecting adware? False = No, True = Yes [Default].

"detect_joke_hoax"
- Should phpMussel parse signatures for detecting joke/hoax malware/viruses? False = No, True = Yes [Default].

"detect_pua_pup"
- Should phpMussel parse signatures for detecting PUAs/PUPs? False = No, True = Yes [Default].

"detect_packer_packed"
- Should phpMussel parse signatures for detecting packers and packed data? False = No, True = Yes [Default].

"detect_shell"
- Should phpMussel parse signatures for detecting shell scripts? False = No, True = Yes [Default].

"detect_deface"
- Should phpMussel parse signatures for detecting defacements and defacers? False = No, True = Yes [Default].

####"files" (Category)
File handling configuration.

"max_uploads"
- Maximum allowable number of files to scan during files upload scan before aborting the scan and informing the user they are uploading too much at once! Provides protection against a theoretical attack whereby an attacker attempts to DDoS your system or CMS by overloading phpMussel to slow down the PHP process to a grinding halt. Recommended: 10. You may wish to raise or lower this number depending on the speed of your hardware. Note that this number doesn't account for or include the contents of archives.

"filesize_limit"
- Filesize limit in KB. 65536 = 64MB [Default], 0 = No limit (always greylisted), any (positive) numeric value accepted. This can be useful when your PHP configuration limits the amount of memory a process can hold or if your PHP configuration limits filesize of uploads.

"filesize_response"
- What to do with files that exceed the filesize limit (if one exists). 0 - Whitelist, 1 - Blacklist [Default].

"filetype_whitelist", "filetype_blacklist", "filetype_greylist"
- If your system only allows specific types of files to be uploaded, or if your system explicitly denies certain types of files, specifying those filetypes in whitelists, blacklists and greylists can increase the speed at which scanning is performed by allowing the script to skip over certain filetypes. Format is CSV (comma separated values). If you want to scan everything, rather than whitelist, blacklist or greylist, leave the variable(/s) blank; Doing so will disable whitelist/blacklist/greylist.
- Logical order of processing is:
  - If the filetype is whitelisted, don't scan and don't block the file, and don't check the file against the blacklist or the greylist.
  - If the filetype is blacklisted, don't scan the file but block it anyway, and don't check the file against the greylist.
  - If the greylist is empty or if the greylist is not empty and the filetype is greylisted, scan the file as per normal and determine whether to block it based on the results of the scan, but if the greylist is not empty and the filetype is not greylisted, treat the file as blacklisted, therefore not scanning it but blocking it anyway.

"check_archives"
- Attempt to check the contents of archives? 0 - No (do not check), 1 - Yes (check) [Default].
- Currently, only checking of BZ, GZ, LZF and ZIP files is supported (checking of RAR, CAB, 7z and etcetera not currently supported).
- This is not foolproof! While I highly recommend keeping this turned on, I can't guarantee it'll always find everything.
- Also be aware that archive checking currently is not recursive for ZIPs.

"filesize_archives"
- Carry over filesize blacklisting/whitelisting to the contents of archives? 0 - No (just greylist everything), 1 - Yes [Default].

"filetype_archives"
- Carry over filetype blacklisting/whitelisting to the contents of archives? 0 - No (just greylist everything) [Default], 1 - Yes.

"max_recursion"
- Maximum recursion depth limit for archives. Default = 10.

"block_encrypted_archives"
- Detect and block encrypted archives? Because phpMussel isn't able to scan the contents of encrypted archives, it's possible that archive encryption may be employed by an attacker as a means of attempting to bypass phpMussel, anti-virus scanners and other such protections. Instructing phpMussel to block any archives that it discovers to be encrypted could potentially help reduce any risk associated with these such possibilities. 0 - No, 1 - Yes [Default].

####"attack_specific" (Category)
Attack-specific directives.

Chameleon attack detection: 0 = Off, 1 = On.

"chameleon_from_php"
- Search for PHP header in files that are neither PHP files nor recognised archives.

"chameleon_from_exe"
- Search for executable headers in files that are neither executables nor recognised archives and for executables whose headers are incorrect.

"chameleon_to_archive"
- Search for archives whose headers are incorrect (Supported: BZ, GZ, RAR, ZIP, RAR, GZ).

"chameleon_to_doc"
- Search for office documents whose headers are incorrect (Supported: DOC, DOT, PPS, PPT, XLA, XLS, WIZ).

"chameleon_to_img"
- Search for images whose headers are incorrect (Supported: BMP, DIB, PNG, GIF, JPEG, JPG, XCF, PSD, PDD, WEBP).

"chameleon_to_pdf"
- Search for PDF files whose headers are incorrect.

"archive_file_extensions" and "archive_file_extensions_wc"
- Recognised archive file extensions (format is CSV; should only add or remove when problems occur; unnecessarily removing may cause false-positives to appear for archive files, whereas unnecessarily adding will essentially whitelist what you're adding from attack specific detection; modify with caution; also note that this has no effect on what archives can and can't be analysed at content-level). The list, as is at default, lists those formats used most commonly across the majority of systems and CMS, but intentionally isn't necessarily comprehensive.

"general_commands"
- Search content of files for general commands such as `eval()`, `exec()` and `include()`? 0 - No (do not check) [Default], 1 - Yes (check). Disable this option if you intend to upload any of the following to your system or CMS via your browser: PHP, JavaScript, HTML, python, perl files and etcetera. Enable this option if you don't have any additional protections on your system and do not intend to upload such files. If you use additional security in conjunction with phpMussel such as ZB Block, there is no need to turn this option on, because most of what phpMussel will look for (in the context of this option) are duplications of protections that are already provided.

"block_control_characters"
- Block any files containing any control characters (other than newlines)? (`[\x00-\x08\x0b\x0c\x0e\x1f\x7f]`) If you're _**ONLY**_ uploading plain-text, then you can turn this option on to provide some additional protection to your system. However, if you upload anything other than plain-text, turning this on may result in false positives. 0 - Don't block [Default], 1 - Block.

"corrupted_exe"
- Corrupted files and parse errors. 0 = Ignore, 1 = Block [Default]. Detect and block potentially corrupted PE (Portable Executable) files? Often (but not always), when certain aspects of a PE file are corrupted or can't be parsed correctly, it can be indicative of a viral infection. The processes used by most anti-virus programs to detect viruses in PE files require parsing those files in certain ways, which, if the programmer of a virus is aware of, will specifically try to prevent, in order to allow their virus to remain undetected.

"decode_threshold"
- Optional limitation or threshold to the length of raw data within which decode commands should be detected (in case there are any noticeable performance issues whilst scanning). Value is an integer representing filesize in KB. Default = 512 (512KB). Zero or null value disables the threshold (removing any such limitation based on filesize).

"scannable_threshold"
- Optional limitation or threshold to the length of raw data that phpMussel is permitted to read and scan (in case there are any noticeable performance issues whilst scanning). Value is an integer representing filesize in KB. Default = 32768 (32MB). Zero or null value disables the threshold. Generally, this value shouldn't be less than the average filesize of file uploads that you want and expect to receive to your server or website, shouldn't be more than the filesize_limit directive, and shouldn't be more than roughly one fifth of the total allowable memory allocation granted to PHP via the php.ini configuration file. This directive exists to try to prevent phpMussel from using up too much memory (that'd prevent it from being able to successfully scan files above a certain filesize).

####"compatibility" (Category)
Compatibility directives for phpMussel.

"ignore_upload_errors"
- This directive should generally be disabled unless it's required for correct functionality of phpMussel on your specific system. Normally, when disabled, when phpMussel detects the presence of elements in the `$_FILES` array(), it'll attempt to initiate a scan of the files that those elements represent, and, if those elements are blank or empty, phpMussel will return an error message. This is proper behaviour for phpMussel. However, for some CMS, empty elements in `$_FILES` can occur as a result of the natural behaviour of those CMS, or errors may be reported when there aren't any, in which case, the normal behaviour for phpMussel will be interfering with the normal behaviour of those CMS. If such a situation occurs for you, enabling this option will instruct phpMussel to not attempt to initiate scans for such empty elements, ignore them when found and to not return any related error messages, thus allowing continuation of the page request. 0 - OFF, 1 - ON.

"only_allow_images"
- If you only expect or only intend to allow images to be uploaded to your system or CMS, and if you absolutely don't require any files other than images to be uploaded to your system or CMS, this directive should be enabled, but should otherwise be disabled. If this directive is enabled, it'll instruct phpMussel to indiscriminately block any uploads identified as non-image files, without scanning them. This may reduce processing time and memory usage for attempted uploads of non-image files. 0 - OFF, 1 - ON.

####"heuristic" (Category)
Heuristic directives.

"threshold"
- There are certain signatures of phpMussel that are intended to identify suspicious and potentially malicious qualities of files being uploaded without in themselves identifying those files being uploaded specifically as being malicious. This "threshold" value tells phpMussel what the maximum total weight of suspicious and potentially malicious qualities of files being uploaded that's allowable is before those files are to be flagged as malicious. The definition of weight in this context is the total number of suspicious and potentially malicious qualities identified. By default, this value will be set to 3. A lower value generally will result in a higher occurrence of false positives but a higher number of malicious files being flagged, whereas a higher value generally will result in a lower occurrence of false positives but a lower number of malicious files being flagged. It's generally best to leave this value at its default unless you're experiencing problems related to it.

####"virustotal" (Category)
VirusTotal.com directives.

"vt_public_api_key"
- Optionally, phpMussel is able to scan files using the Virus Total API as a way to provide a greatly enhanced level of protection against viruses, trojans, malware and other threats. By default, scanning files using the Virus Total API is disabled. To enable it, an API key from Virus Total is required. Due to the significant benefit that this could provide to you, it's something that I highly recommend enabling. Please be aware, however, that to use the Virus Total API, you _**MUST**_ agree to their Terms of Service and you _**MUST**_ adhere to all guidelines as per described by the Virus Total documentation! You are NOT permitted to use this integration feature UNLESS:
  - You have read and agree to the Terms of Service of Virus Total and its API. The Terms of Service of Virus Total and its API can be found [Here](https://www.virustotal.com/en/about/terms-of-service/).
  - You have read and you understand, at a minimum, the preamble of the Virus Total Public API documentation (everything after "VirusTotal Public API v2.0" but before "Contents"). The Virus Total Public API documentation can be found [Here](https://www.virustotal.com/en/documentation/public-api/).

Note: If scanning files using the Virus Total API is disabled, you won't need to review any of the directives in this category (`virustotal`), because none of them will do anything if this is disabled. To acquire a Virus Total API key, from anywhere on their website, click the "Join our Community" link located towards the top-right of the page, enter in the information requested, and click "Sign up" when done. Follow all instructions supplied, and when you've got your public API key, copy/paste that public API key to the `vt_public_api_key` directive of the `phpmussel.ini` configuration file.

"vt_suspicion_level"
- By default, phpMussel will restrict which files it scans using the Virus Total API to those files that it considers "suspicious". You can optionally adjust this restriction by changing the value of the `vt_suspicion_level` directive.
- `0`: Files are only considered suspicious if, upon being scanned by phpMussel using its own signatures, they are deemed to carry a heuristic weight. This would effectively mean that use of the Virus Total API would be for a second opinion for when phpMussel suspects that a file may potentially be malicious, but can't entirely rule out that it may also potentially be benign (non-malicious) and therefore would otherwise normally not block it or flag it as being malicious.
- `1`: Files are considered suspicious if, upon being scanned by phpMussel using its own signatures, they are deemed to carry a heuristic weight, if they're known to be executable (PE files, Mach-O files, ELF/Linux files, etc), or if they're known to be of a format that could potentially contain executable data (such as executable macros, DOC/DOCX files, archive files such as RARs, ZIPS and etc). This is the default and recommended suspicion level to apply, effectively meaning that use of the Virus Total API would be for a second opinion for when phpMussel doesn't initially find anything malicious or wrong with a file that it considers to be suspicious and therefore would otherwise normally not block it or flag it as being malicious.
- `2`: All files are considered suspicious and should be scanned using the Virus Total API. I don't generally recommend applying this suspicion level, due to the risk of reaching your API quota much quicker than would otherwise be the case, but there are certain circumstances (such as when the webmaster or hostmaster has very little faith or trust whatsoever in any of the uploaded content of their users) where this suspicion level could be appropriate. With this suspicion level, all files not normally blocked or flagged as being malicious would be scanned using the Virus Total API. Note, however, that phpMussel will cease using the Virus Total API when your API quota has been reached (regardless of suspicion level), and that your quota will likely be reached much faster when using this suspicion level.

Note: Regardless of suspicion level, any files that are either blacklisted or whitelisted by phpMussel won't be scanned using the Virus Total API, because those such files would've already been declared as either malicious or benign by phpMussel by the time that they would've otherwise been scanned by the Virus Total API, and therefore, additional scanning wouldn't be required. The ability of phpMussel to scan files using the Virus Total API is intended to build further confidence for whether a file is malicious or benign in those circumstances where phpMussel itself isn't entirely certain as to whether a file is malicious or benign.

"vt_weighting"
- Should phpMussel apply the results of scanning using the Virus Total API as detections or as detection weighting? This directive exists, because, although scanning a file using multiple engines (as Virus Total does) should result in an increased detection rate (and therefore in a higher number of malicious files being caught), it can also result in a higher number of false positives, and therefore, in some circumstances, the results of scanning may be better utilised as a confidence score rather than as a definitive conclusion. If a value of 0 is used, the results of scanning using the Virus Total API will be applied as detections, and therefore, if any engine used by Virus Total flags the file being scanned as being malicious, phpMussel will consider the file to be malicious. If any other value is used, the results of scanning using the Virus Total API will be applied as detection weighting, and therefore, the number of engines used by Virus Total that flag the file being scanned as being malicious will serve as a confidence score (or detection weighting) for whether or not the file being scanned should be considered malicious by phpMussel (the value used will represent the minimum confidence score or weight required in order to be considered malicious). A value of 0 is used by default.

"vt_quota_rate" and "vt_quota_time"
- According to the Virus Total API documentation, "it is limited to at most 4 requests of any nature in any given 1 minute time frame. If you run a honeyclient, honeypot or any other automation that is going to provide resources to VirusTotal and not only retrieve reports you are entitled to a higher request rate quota". By default, phpMussel will strictly adhere to these limitations, but due to the possibility of these rate quotas being increased, these two directives are provided as a means for you to instruct phpMussel as to what limit it should adhere to. Unless you've been instructed to do so, it's not recommended for you to increase these values, but, if you've encountered problems relating to reaching your rate quota, decreasing these values _**MAY**_ sometimes help you in dealing with these problems. Your rate limit is determined as `vt_quota_rate` requests of any nature in any given `vt_quota_time` minute time frame.

####"template_data" (Category)
Directives/Variables for templates and themes.

Template data relates to the HTML output used to generate the "Upload Denied" message displayed to users upon a file upload being blocked. If you're using custom themes for phpMussel, HTML output is sourced from the `template_custom.html` file, and otherwise, HTML output is sourced from the `template.html` file. Variables written to this section of the configuration file are parsed to the HTML output by way of replacing any variable names circumfixed by curly brackets found within the HTML output with the corresponding variable data. For example, where `foo="bar"`, any instance of `<p>{foo}</p>` found within the HTML output will become `<p>bar</p>`.

"css_url"
- The template file for custom themes utilises external CSS properties, whereas the template file for the default theme utilises internal CSS properties. To instruct phpMussel to use the template file for custom themes, specify the public HTTP address of your custom theme's CSS files using the `css_url` variable. If you leave this variable blank, phpMussel will use the template file for the default theme.

---


###7. <a name="SECTION7"></a>ĐỊNH DẠNG CỦA CHỬ KÝ

####*FILENAME SIGNATURES*
All filename signatures follow the format:

`NAME:FNRX`

Where NAME is the name to cite for that signature and FNRX is the regex pattern to match filenames (unencoded) against.

####*MD5 SIGNATURES*
All MD5 signatures follow the format:

`HASH:FILESIZE:NAME`

Where HASH is the MD5 hash of an entire file, FILESIZE is the total size of that file and NAME is the name to cite for that signature.

####*ARCHIVE METADATA SIGNATURES*
All archive metadata signatures follow the format:

`NAME:FILESIZE:CRC32`

Where NAME is the name to cite for that signature, FILESIZE is the total size (uncompressed) of a file contained within the archive and CRC32 is the CRC32 checksum of that contained file.

####*PE SECTIONAL SIGNATURES*
All PE Sectional signatures follow the format:

`SIZE:HASH:NAME`

Where HASH is the MD5 hash of a section of a PE file, SIZE is the total size of that section and NAME is the name to cite for that signature.

####*PE EXTENDED SIGNATURES*
All PE extended signatures follow the format:

`$VAR:HASH:SIZE:NAME`

Where $VAR is the name of the PE variable to match against, HASH is the MD5 hash of that variable, SIZE is the total size of that variable and NAME is the name to cite for that signature.

####*WHITELIST SIGNATURES*
All Whitelist signatures follow the format:

`HASH:FILESIZE:TYPE`

Where HASH is the MD5 hash of an entire file, FILESIZE is the total size of that file and TYPE is the type of signatures the whitelisted file is to be immune against.

####*COMPLEX EXTENDED SIGNATURES*
Complex Extended signatures are rather different to the other types of signatures possible with phpMussel, in that what they are matching against is specified by the signatures themselves and they can match against multiple criteria. The match criterias are delimited by ";" and the match type and match data of each match criteria is delimited by ":" as so that format for these signatures tends to look a bit like:

`$variable1:SOMEDATA;$variable2:SOMEDATA;SignatureName`

####*EVERYTHING ELSE*
All other signatures follow the format:

`NAME:HEX:FROM:TO`

Where NAME is the name to cite for that signature and HEX is a hexadecimal-encoded segment of the file intended to be matched by the given signature. FROM and TO are optional parameters, indicting from which and to which positions in the source data to check against (not supported by the mail function).

####*REGEX*
Any form of regex understood and correctly processed by PHP should also be correctly understood and processed by phpMussel and its signatures. However, I'd suggest taking extreme caution when writing new regex based signatures, because, if you're not entirely sure what you're doing, there can be highly irregular and/or unexpected results. Take a look at the phpMussel source-code if you're not entirely sure about the context in which regex statements are parsed. Also, remember that all patterns (with exception to filename, archive metadata and MD5 patterns) must be hexadecimally encoded (foregoing pattern syntax, of course)!

####*WHERE TO PUT CUSTOM SIGNATURES?*
Only put custom signatures in those files intended for custom signatures. Those files should contain "_custom" in their filenames. You should also avoid editing the default signature files, unless you know exactly what you're doing, because, aside from being good practise in general and aside from helping you distinguish between your own signatures and the default signatures included with phpMussel, it's good to stick to editing only the files intended for editing, because tampering with the default signature files can cause them to stop working correctly, due to the "maps" files: The maps files tell phpMussel where in the signature files to look for signatures required by phpMussel as per when required, and these maps can become out-of-sync with their associated signature files if those signature files are tampered with. You can put pretty much whatever you want into your custom signatures, so long as you follow the correct syntax. However, be careful to test new signatures for false-positives beforehand if you intend to share them or use them in a live environment.

####*SIGNATURE BREAKDOWN*
The following is a breakdown of the types of signatures used by phpMussel:
- "Normalised ASCII Signatures" (ascii_*). Checked against the contents of every non-whitelisted file targeted for scanning.
- "Complex Extended Signatures" (coex_*). Mixed signature type matching.
- "ELF Signatures" (elf_*). Checked against the contents of every non-whitelisted file targeted for scanning and matched to the ELF format.
- "Portable Executable Signatures" (exe_*). Checked against the contents of every non-whitelisted targeted for scanning and matched to the PE format.
- "Filename Signatures" (filenames_*). Checked against the filenames of files targeted for scanning.
- "General Signatures" (general_*). Checked against the contents of every non-whitelisted file targeted for scanning.
- "Graphics Signatures" (graphics_*). Checked against the contents of every non-whitelisted file targeted for scanning and matched to a known graphical file format.
- "General Commands" (hex_general_commands.csv). Checked against the contents of every non-whitelisted file targeted for scanning.
- "Normalised HTML Signatures" (html_*). Checked against the contents of every non-whitelisted HTML file targeted for scanning.
- "Mach-O Signatures" (macho_*). Checked against the contents of every non-whitelisted file targeted for scanning and matched to the Mach-O format.
- "Email Signatures" (mail_*). Checked against the $body variable parsed to the phpMussel_mail() function, which is intended to be the body of email messages or similar entities (potentially forum posts and etcetera).
- "MD5 Signatures" (md5_*). Checked against the MD5 hash of the contents and the filesize of every non-whitelisted file targeted for scanning.
- "Archive Metadata Signatures" (metadata_*). Checked against the CRC32 hash and filesize of the initial file contained inside of any non-whitelisted archive targeted for scanning.
- "OLE Signatures" (ole_*). Checked against the contents of every non-whitelisted OLE object targeted for scanning.
- "PDF Signatures" (pdf_*). Checked against the contents of every non-whitelisted PDF file targeted for scanning.
- "Portable Executable Sectional Signatures" (pe_*). Checked against the MD5 hash and the size of each PE section of every non-whitelisted file targeted for scanning and matched to the PE format.
- "Portable Executable Extended Signatures" (pex_*). Checked against the MD5 hash and the size of variables within every non-whitelisted file targeted for scanning and matched to the PE format.
- "SWF Signatures" (swf_*). Checked against the contents of every non-whitelisted Shockwave file targeted for scanning.
- "Whitelist Signatures" (whitelist_*). Checked against the MD5 hash of the contents and the filesize of every file targeted for scanning. Matched files will be immune to being matched by the type of signature mentioned in their whitelist entry.
- "XML/XDP-Chunk Signatures" (xmlxdp_*). Checked against any XML/XDP chunks found within any non-whitelisted files targeted for scanning.
(Note that any of these signatures may be easily disabled via `phpmussel.ini`).

---


###8. <a name="SECTION8"></a>NHỮNG VẤN ĐỀ HỢP TƯƠNG TÍCH

####PHP và PCRE
- phpMussel cần PHP và PCRE để thực hiện và hoạt động. Nếu không có PHP, hoạc không có PCRE thêm của PHP, phpMussel sẽ không thực hiện và hoạt động bình thường. Bạn nên chắc chắc rằng hệ thống của bạn có PHP và PCRE cài vào và có sẵn trước khi tải và cài đặt phpMussel.

####KHẢ NĂNG TƯƠNG THÍCH PHẦN MỀM CHỐNG VIRUS

Cho hầu hết các phần, phpMussel sẽ tương hợp với hầu hết các phần mềm quét virus khác. Nhưng mà, có một số người sử dụng trong quá khứ đã báo cáo một số vấn đề. Thông tin dưới đây là từ VirusTotal.com, và nó miêu tả một số giả tích cực báo cáo bởi các chương trình chống virus khác nhau chống phpMussel. Mặc dù thông tin này không đảm bảo nếu bạn gặp phải vấn đề tương hợp giữa phpMussel và phần mềm chống virus của bạn, nếu phần mềm chống virus của bạn được ghi nhận là cách gắn cờ chống lại phpMussel, bạn nên tắt nó trước khi sử dụng phpMussel hoặc nên xét các lựa chọn khác cho một trong hai phần mềm chống virus của bạn hoặc phpMussel.

Thông tin này được cập nhật lần cứơi vào ngày 7 Tháng Chín 2015 và có thể áp dụng cho phpMussel công bố hai loại phiên bản nhỏ mới nhất (v0.6-v0.7a) vào thời gian cái này được viết.

| Chương trình quét    |  Kết quả                             |
|----------------------|--------------------------------------|
| Ad-Aware             |  Không có vấn đề                     |
| Agnitum              |  Không có vấn đề                     |
| AhnLab-V3            |  Không có vấn đề                     |
| AntiVir              |  Không có vấn đề                     |
| Antiy-AVL            |  Không có vấn đề                     |
| Avast                |  Báo cáo "JS:ScriptSH-inf [Trj]"     |
| AVG                  |  Không có vấn đề                     |
| Baidu-International  |  Không có vấn đề                     |
| BitDefender          |  Không có vấn đề                     |
| Bkav                 |  Báo cáo "VEXDAD2.Webshell"          |
| ByteHero             |  Không có vấn đề                     |
| CAT-QuickHeal        |  Không có vấn đề                     |
| ClamAV               |  Không có vấn đề                     |
| CMC                  |  Không có vấn đề                     |
| Commtouch            |  Không có vấn đề                     |
| Comodo               |  Không có vấn đề                     |
| DrWeb                |  Không có vấn đề                     |
| Emsisoft             |  Không có vấn đề                     |
| ESET-NOD32           |  Không có vấn đề                     |
| F-Prot               |  Không có vấn đề                     |
| F-Secure             |  Không có vấn đề                     |
| Fortinet             |  Không có vấn đề                     |
| GData                |  Không có vấn đề                     |
| Ikarus               |  Không có vấn đề                     |
| Jiangmin             |  Không có vấn đề                     |
| K7AntiVirus          |  Không có vấn đề                     |
| K7GW                 |  Không có vấn đề                     |
| Kaspersky            |  Không có vấn đề                     |
| Kingsoft             |  Không có vấn đề                     |
| Malwarebytes         |  Không có vấn đề                     |
| McAfee               |  Báo cáo "New Script.c"              |
| McAfee-GW-Edition    |  Báo cáo "New Script.c"              |
| Microsoft            |  Không có vấn đề                     |
| MicroWorld-eScan     |  Không có vấn đề                     |
| NANO-Antivirus       |  Không có vấn đề                     |
| Norman               |  Không có vấn đề                     |
| nProtect             |  Không có vấn đề                     |
| Panda                |  Không có vấn đề                     |
| Qihoo-360            |  Không có vấn đề                     |
| Rising               |  Không có vấn đề                     |
| Sophos               |  Không có vấn đề                     |
| SUPERAntiSpyware     |  Không có vấn đề                     |
| Symantec             |  Không có vấn đề                     |
| TheHacker            |  Không có vấn đề                     |
| TotalDefense         |  Không có vấn đề                     |
| TrendMicro           |  Không có vấn đề                     |
| TrendMicro-HouseCall |  Không có vấn đề                     |
| VBA32                |  Không có vấn đề                     |
| VIPRE                |  Không có vấn đề                     |
| ViRobot              |  Không có vấn đề                     |


---


Lần cuối cập nhật: 11 Tháng Chín 2015 (2015.09.11).

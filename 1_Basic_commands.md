# Basic Linux commands

[Read the Docs](https://www.hostinger.com/tutorials/linux-commands)

## ls: Listing Directory

|         Command         | Description                                                              |
| :---------------------: | ------------------------------------------------------------------------ |
|          `ls`           | Liệt kê tất cả các file và folder có trong thư mục ở trạng thái hiện hữu |
|       `ls home/`        | Liệt kê tất cả các file và folder có trong thư mục tùy chọn              |
|         `ls -l`         | Liệt kê chi tiết (người tạo, quyền hạn, dung lượng, ngày tạo,...)        |
|         `ls -a`         | Liệt kê file và folder ở trạng thái ẩn và hiện hữu                       |
| `ls -la` <br/> `ls -al` | Liệt kê chi tiết file và folder ở trạng thái ẩn và hiện hữu              |
|         `ls -R`         | Hiện cả cấp con của thư mục được list ra                                 |

## cd: Change Directory

|        Command        | Description                    |
| :-------------------: | ------------------------------ |
|   `cd /` <br/> `cd`   | Trở về thư mục root            |
|      `cd home/`       | Vào thư mục home               |
|   `cd home/reactjs`   | Vào thư mục reactjs trong home |
| `cd -` <br/> `cd ../` | Back về thư mục cha            |

## clear: clear old commands

\- Just use `clear` or `Ctrl+L`

## mkdir: Create a directory

|                      Command                      | Description                     |
| :-----------------------------------------------: | ------------------------------- |
|                  `mkdir parent`                   | Tạo mới thư mục parent          |
| `mkdir pr/ch1/ch2 -p` <br/> `mkdir -p pr/ch1/ch2` | Tạo 1 dãy các thư mục lồng nhau |

## touch: Create new file

|        Command        | Description                          |
| :-------------------: | ------------------------------------ |
|  `touch index.html`   | Tạo mới 1 file                       |
| `touch pr/index.html` | Tạo mới 1 file vào bên trong thư mục |

## rmdir & rm: Remove a directory

|         Command         | Description                     |
| :---------------------: | ------------------------------- |
|      `rmdir home/`      | Xóa thư mục rỗng                |
| `rm file.ext file2.ext` | Xóa nhiều file                  |
|    `rm -r home/src/`    | Xóa 1 dãy các thư mục lồng nhau |

## nano: Read & write file

|     Command     | Description                   |
| :-------------: | ----------------------------- |
| `nano file.ext` | Bật file để chỉnh sửa với GNU |

## cat: Get file content and merge

|            Command            | Description                                        |
| :---------------------------: | -------------------------------------------------- |
|      `cat filename.ext`       | In ra màn hình nội dung của file                   |
|   `cat file1.ext file2.ext`   | In ra màn hình nội dung lần lươt của từng của file |
| `cat f1.ext f2.ext > new.txt` | Gộp nội dung của 2 file và tạo thành 1 file mới    |

## echo: Overwrite and append file content

|           Command           | Description                                      |
| :-------------------------: | ------------------------------------------------ |
|      `echo "content"`       | In ra màn hình nội dung trong ""                 |
| `echo "content" > new.txt`  | Tạo mới (nếu chưa) và ghi đè nội dung trong file |
| `echo "content" >> new.txt` | Ghi nội dung vào phần sau cùng của file          |

## tail: Reading the last line of file

|       Command        | Description                   |
| :------------------: | ----------------------------- |
|   `tail file.ext`    | In ra 10 dòng cuối của file   |
| `tail -n 5 file.ext` | In ra 5 dòng cuối của file    |
|  `tail -f file.ext`  | Theo dõi file nếu có thay đổi |

## grep: Find a specific content in file

|                             Command                             | Description                                 |
| :-------------------------------------------------------------: | ------------------------------------------- |
| `grep "content" file.ext` <br/>`cat file.ext \| grep "content"` | Tìm kiếm các dòng có chứa nội dung trong "" |
|                  `grep -w "content" file.ext`                   | Tìm kiếm khớp hoàn toàn                     |
|                  `grep -i "content" file.ext`                   | Tìm kiếm không phân biệt HOA thường         |
|                  `grep -c "content" file.ext`                   | Đếm số lượng kết quả trùng khớp             |
|                  `grep -n "content" file.ext`                   | Hiện số dòng chứa kết quả trùng khớp        |
|                       `ls \| grep ".js"`                        | Tìm tất cả file có ext là 'js'              |

## cp: Copy a file to another directory

|              Command              | Description                               |
| :-------------------------------: | ----------------------------------------- |
|     `cp file.ext newFile.ext`     | Sao chép file                             |
| `cp pr1/file.ext pr2/newFile.ext` | Sao chép file của folder sang folder khác |
|          `cp -r pr1 pr2`          | Sao chép folder                           |

## mv: Move a file

|            Command            | Description                 |
| :---------------------------: | --------------------------- |
|   `mv file.ext newFile.ext`   | Đổi tên file                |
| `mv file.ext pr1/newFile.ext` | Di chuyển file và đổi tên   |
|       `mv pr1 pr2/pr3`        | Di chuyển folder và đổi tên |

## help: Open guide of specific command

\- Add `--help` at the end like `cd --help` `tail --help` `ls --help`

## chmod: change permissions for read, write, and execute

[Docs](https://www.computerhope.com/unix/uchmod.htm#view-permissions)

[Video](https://fullstack.edu.vn/learning/windows-terminal-wsl?id=d31b1650-0809-4c51-b3d6-99a66494622a)

## kill: stop unresponsive program

[Docs](https://www.hostinger.com/tutorials/linux-commands)

|    Command    | Description                                             |
| :-----------: | ------------------------------------------------------- |
|   `ps aux`    | Liệt kê các tiến trình đang thực thi => PID             |
|  `kill 1068`  | Dừng chương trình với mã PID => gửi request và save all |
| `kill 9 1068` | Dừng chương trình ngay lập tức                          |

## ping: check connectivity status to a server

|      Command      | Description                        |
| :---------------: | ---------------------------------- |
| `ping google.com` | Kiểm tra kết nối tới server google |

## uname: check Unix Name

|  Command   | Description                                       |
| :--------: | ------------------------------------------------- |
|  `uname`   | Hiển thị thông tin hệ điều hành hiện tại          |
| `uname -a` | Hiển thị chi tiết thông tin hệ điều hành hiện tại |

## passwd: change password of user

| Command  | Description                      |
| :------: | -------------------------------- |
| `passwd` | Đổi mật khẩu người dùng hiện tại |

## df: report system’s disk space usage

| Command | Description                                        |
| :-----: | -------------------------------------------------- |
|  `df`   | Hiển thị thông tin dung lượng của ổ cứng (theo KB) |
| `df -h` | Hiển thị cho con người dễ đọc                      |
| `df -m` | Hiển thị theo MB                                   |

## Other tips

|         Command          | Description                                               |
| :----------------------: | --------------------------------------------------------- |
|          `tab`           | Auto complete                                             |
|        `tab tab`         | Hiện thị tất cả file thư mục khi cd                       |
|        `ctrl + a`        | Di chuyển con trỏ về đầu dòng                             |
|        `ctrl + e`        | Di chuyển con trỏ về cuối dòng                            |
|  `command-1;command-2`   | Chạy đồng thời nhiều command (không phân biệt hoàn thành) |
| `command-1 && command-2` | Chỉ chạy command phía sau khi command trước hoàn thành    |

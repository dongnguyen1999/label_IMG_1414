# Yolo_mark
**Windows** & **Linux** GUI for marking bounded boxes of objects in images for training Yolo v3 and v2

* To compile on **Windows** open `yolo_mark.sln` in MSVS2013/2015, compile it **x64 & Release** and run the file: `x64/Release/yolo_mark.cmd`. Change paths in `yolo_mark.sln` to the OpenCV 2.x/3.x installed on your computer:

    * (right click on project) -> properties -> C/C++ -> General -> Additional Include Directories: `C:\opencv_3.0\opencv\build\include;`
        
    * (right click on project) -> properties -> Linker -> General -> Additional Library Directories: `C:\opencv_3.0\opencv\build\x64\vc14\lib;`

* To compile on **Linux** type in console 3 commands:
    ```
    cmake .
    make
    ./linux_mark.sh
    ```

Supported both: OpenCV 2.x and OpenCV 3.x

--------

1. To test, simply run 
  * **on Windows:** `x64/Release/yolo_mark.cmd`
  * **on Linux:** `./linux_mark.sh`

### Instruction manual

#### Mouse control

Button | Description | 
--- | --- |
Left | Draw box
Right | Move box

#### Keyboard Shortcuts

Shortcut | Description | 
--- | --- |
<kbd>→</kbd> | Next image |
<kbd>←</kbd> | Previous image |
<kbd>r</kbd> | Delete selected box (mouse hovered) |
<kbd>c</kbd> | Clear all marks on the current image |
<kbd>p</kbd> | Copy previous mark |
<kbd>o</kbd> | Track objects |
<kbd>ESC</kbd> | Close application |
<kbd>n</kbd> | One object per image |
<kbd>0-9</kbd> | Object id |
<kbd>m</kbd> | Show coords |
<kbd>w</kbd> | Line width |
<kbd>k</kbd> | Hide object name |
<kbd>h</kbd> | Help |

#### Cách làm:
Compile trên hệ điều hành tương ứng
Chạy ứng dụng

Sử dụng các phím số để thay đổi nhãn: <br>
* Phím 0: Nhãn bike
* Phím 1: Nhãn car 

Chọn nhãn bike, vẽ hợp giới hạn cho tất cả các xe máy <br>
Chọn nhãn car, vẽ hợp giới hạn cho tất cả các xe 4 bánh không bị che khuất quá 70% <br>

Đông gán 100 hình đầu <br>
Dương gán 100 hình sau (từ hình thứ 101 trở đi) <br>



Sau khi gán xong phần của mình: <br>
  ```
  git add .
  git commit -m 'Submit label from ... to ...'
  git push origin master
  ```




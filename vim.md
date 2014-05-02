如来神掌之Vim 
-------------------------------------------
使用说明： 
0.  起势，按/eg -> n到例子1.1.
1.  存活
  1.1.  i在光标插入aaa，Esc退出，a在光标后插入bbb，A在本行尾插入ccc，I在行首插入ddd，o在本行下起一行插入eee，O在本行上另起一行插fff,6u往回退
     eg:
  1.2. 按x删除e,/d到delete,dw删除字，按p复制出，按u往回退，大P会更好,d$删到尾,2dd删2行,按5u都取消
     eg: delete this word and line
     deleted by 2dd 
  1.3. :w 存盘不退出 :wq存退
  1.5. hjkl 移动，上下左右移动
            00000k0
            00hegl0
            00000j0
  1.6. :help i 看一下命令帮助,:q退出
  1.7. eg gg到文首，G到文未,17G再回
  1.8. :%s/holle/hello/g holle换hello, u变回来

2.  感觉良好
  2.1. cw → 替换从光标所在位置后到一个单词结尾的字符 dw只删除
      eg delete then insert
      eg delete only
  2.2.  eg 0 到行头 ^ 到非空头            
        $ 到行尾, g_ 不空尾。
  2.3. eg yy拷贝 p粘贴 
  2.4. eg u取消，Ctrl-r redo
  2.5. eg :e 打开文件在buffer, :bp 回上个，:bn 到下个，:ls 看所有，:b1到第一，:q会全退，
  2.6. eg :w存 :saveas , :x :wq ZZ 保存退出，:q! 不存就退出 :qa!退所有

3.  觉得更好，更强，更快
  3.1. .来重复上一个命令
    eg ywthisword 再按...
  3.2. N<command>重复某个命令N次
    eg ywthisword 再按4P
  3.3. 2dd 删除两行，3p粘贴三次， 100idesu(Esc Esc)(Esc按两次)
  3.4. .  3. 重复一次所有，重三次内部
    eg 100idesu, 按.再3.
  3.5. eg 跳到第几行，gg到第一，G到最后,39G再回来
  3.6. w 到下字开头 e到本字尾 
    eg 按d，再按w，再按e
  3.7. WE到小段
    eg this is a word
       this is a line
  3.8. eg % to({[word]})
  3.9. eg first first eg * # 下一个前一个当前词
  3.10. eg 组合： 0y$ 行头拷贝到行尾,再p
  3.11. ye egthiswordThenP
  3.12. y2/fooCopyBeforefoo  eg foo100foo 
  3.13. v gU大写 gu小写 
    eg work try dvd
  
4.  使用Vim的超能力
  4.1.  eg 0 到行头 $ 到行尾
	eg ^ 到行非blank头 g_ 到本尾非blank            
	eg fa 到下一个a
	eg t, 到逗号前
	eg 3fa a a a 当前行第三个a。
	a a word eg a a F/T向相反
	eg dt" 删除到"
  4.2. v visual模式，<action>a<object> 和 <action>i<object>
	"eg vi" 会选择 eg vi
	"eg va" 会选择 "eg va"
	(eg vi) 会选择 "eg vi"
	(eg va) 会选择 (eg va)
	((eg v2i))) 会选择(eg v2i) 
  4.3.  块操作，典型的操作： 0 <C-v> <C-d> I-- [ESC]
	eg 在这几行前都加上--  ^ 到行头
	<C-v> 开始块操作
	<C-d> 向下移动 (你也可以使用hjkl来移动光标，或是使用%，或是别的)
	I-- [ESC] I是插入，插入“--”，按ESC键来为每一行生效。
  4.4. Insert 模式，<C-p><C-n>自动补齐
	eg work work
  4.5.  宏录制： qa 记录在寄存器 a ,@a replay a, @@ replay最新
	示例：自增1到100 qaYp<C-a>q→
	qa 开始录制 Yp 复制行.
	<C-a> 增加1.  q 停止录制.
	@a → 在1下面写下 2
	@@ → 在2 正面写下3
	现在做 100@@ 会创建新的100行，并把数据增加到 103.
	eg 
	1
  4.6.  可视化选择： v 开始到结束,V 开始行到结束行,<C-v> 开始位到结束位块(在Windows下应该是<C-q>)
	J 把所有的行连接起来(变成一行)
	< 或 >  左右缩进
	= 自动给缩进

  	eg 在所有被选择的行后加上hello ：
	<C-v> 选择
	$ 到行最后 A, 输入字符串，按 ESC。
  4.7. eg :split 上下分屏 :vsplit垂直分屏, :q退出
       eg <C-w>h/j/k/l :其用来切换分屏。
       eg <C-w>_/| : 最大化 (<C-w>| 垂直分屏)
       eg <C-w>+/- : 增减尺寸


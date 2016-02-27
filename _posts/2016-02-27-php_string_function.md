---
layout: post
title:  'php string fuction study'
date:   '2016-02-27 17:21:20'
categories: php
---
#php手册学习
##字符串函数学习
###常用的函数

1. addcslashes--以c语言风格使用反斜线转义字符串中的字符
   string addcslashes ( string $str , string $charlist )
   返回字符串，该字符串在属于参数 charlist 列表中的字符前都加上了反斜线。

2. addslashes--使用反斜线引用字符串
   tring addslashes ( string $str )
   返回字符串，该字符串为了数据库查询语句等的需要在某些字符前加上了反斜线。
   这些字符是单引号、双引号、反斜线（\）与 NUL（NULL 字符）。

3. bin2hex--函数把ascii字符的字符串转换为十六进制值
   string bin2hex ( string $str )
   返回 ASCII 字符串，为参数 str 的十六进制表示。转换使用字节方式，高四位字节优先。

4. chr--返回指定的字符
   string chr ( int $ascii )
   返回相对应于 ascii 所指定的单个字符。
   此函数与 ord() 是互补的。

5. chunk_split--将字符串分割成小块
   string chunk_split ( string $body [, int $chunklen = 76 [, string $end = "\r\n" ]] )
   使用此函数将字符串分割成小块非常有用。
   body
   要分割的字符。
   chunklen
   分割的尺寸。
   end
   行尾序列符号。

6. count_chars--返回字符串所有字符信息
   mixed count_chars ( string $string [, int $mode = 0 ] )
   统计 string 中每个字节值（0..255）出现的次数，使用多种模式返回结果。
   返回值:
   根据不同的 mode，count_chars() 返回下列不同的结果：
   0 - 以所有的每个字节值作为键名，出现次数作为值的数组。
   1 - 与 0 相同，但只列出出现次数大于零的字节值。
   2 - 与 0 相同，但只列出出现次数等于零的字节值。
   3 - 返回由所有使用了的字节值组成的字符串。
   4 - 返回由所有未使用的字节值组成的字符串。

7. crc32--计算一个字符串的crc32多项式
   int crc32 ( string $str )
   用32 位循环冗余多项式生成这个str的校验码,并返回一个（不一定带有符号的）整数。接受时验证，可以检查传输的数据是否完整。
   Warning:
   由于 PHP 的整数是带符号的，所以在 32 位系统上许多 crc32 校验码将返回负整数。 尽管在 64 位上所有 crc32() 的结果将都是正整数。
   因此你需要使用 sprintf() 或 printf() 的“%u”格式符来获取表示无符号 crc32 校验码的字符串。

8. crypt--单向字符串散列
   string crypt ( string $str [, string $salt ] )
   crypt() 返回一个基于标准 UNIX DES 算法或系统上其他可用的替代算法的散列字符串。

9. echo--输出一个或多个字符串
   void echo ( string $arg1 [, string $... ] )
   输出所有参数。
   echo 不是一个函数（它是一个语言结构）， 因此你不一定要使用小括号来指明参数，单引号，双引号都可以。 echo （不像其他语言构造）不表现得像一个函数， 所以不能总是使用一个函数的上下文。 另外，如果你想给echo 传递多个参数， 那么就不能使用小括号。

10.explode--使用一个字符串分割另一个字符串
   array explode ( string $delimiter , string $string [, int $limit ] )
   此函数返回由字符串组成的数组，每个元素都是 string 的一个子串，它们被字符串 delimiter 作为边界点分割出来。
   delimiter:
   边界上的分隔字符。
   string:
   输入的字符串。
   limit:
   如果设置了 limit 参数并且是正数，则返回的数组包含最多 limit 个元素，而最后那个元素将包含 string 的剩余部分。
   如果 limit 参数是负数，则返回除了最后的 -limit 个元素外的所有元素。
   如果 limit 是 0，则会被当做 1。
   返回值:
   此函数返回由字符串组成的 array，每个元素都是 string 的一个子串，它们被字符串 delimiter 作为边界点分割出来。
   如果 delimiter 为空字符串（""），explode() 将返回 FALSE。 如果 delimiter 所包含的值在 string 中找不到，并且使用了负数的 limit ， 那么会返回空的 array， 否则返回包含 string 单个元素的数组。

11.fprintf--将格式化后的字符串写入到流
   int fprintf ( resource $handle , string $format [, mixed $args [, mixed $... ]] )
   写入一个根据 format 格式化后的字符串到 由 handle 句柄打开的流中。
   handle
   文件系统指针，是典型地由 fopen() 创建的 resource(资源)。
   format
   参见 sprintf() 中对 format 的描述。
   返回值
   返回写入的字符串长度。

12.hex2bin--转换十六进制字符串为二进制字符串

13.html_entity_decode--把html实体转换为字符
   string html_entity_decode ( string $string [, int $flags = ENT_COMPAT | ENT_HTML401 [, string $encoding = ini_get("default_charset") ]] )

14.htmlentities--把字符转换为html实体

15.htmlspecialchars_decode()    把一些预定义的 HTML 实体转换为字符。

16.htmlspecialchars()  把一些预定义的字符转换为 HTML 实体。

17.implode— 将一个一维数组的值转化为字符串
   string implode ( string $glue , array $pieces )
   string implode ( array $pieces )
   用 glue 将一维数组的值连接为一个字符串。
   glue
   默认为空的字符串。
   pieces
   你想要转换的数组。
   返回值
   返回一个字符串，其内容为由 glue 分割开的数组的值。

18.lcfirst — 使一个字符串的第一个字符小写
   string lcfirst ( string $str )
   返回str的第一个字符小写了的字符串。如果str的第一个字符是字母，则将其转换为小写。

19.ltrim — 删除字符串开头的空白字符（或其他字符）
   string ltrim ( string $str [, string $character_mask ] )
   删除字符串开头的空白字符（或其他字符）
   str:
   输入的字符串。
   character_mask:
   通过参数 character_mask，你也可以指定想要删除的字符，简单地列出你想要删除的所有字符即可。使用..，可以指定字符的范围。

20.md5 — 计算字符串的 MD5 散列值
   说明
   string md5 ( string $str [, bool $raw_output = false ] )
   使用 » RSA 数据安全公司的 MD5 报文算法计算 str 的 MD5 散列值。

21.md5_file — 计算指定文件的 MD5 散列值
   string md5_file ( string $filename [, bool $raw_output = false ] )
   使用 » RSA 数据安全公司的 MD5 报文算法计算 filename 文件的 MD5 散列值并返回。该散列值为 32 字符的十六进制数字。
   raw_output
   如果被设置为 TRUE，那么报文摘要将以原始的 16 位二进制格式返回

22.nl2br — 在字符串所有新行之前插入 HTML 换行标记
   string nl2br ( string $string [, bool $is_xhtml = true ] )
   在字符串 string 所有新行之前插入 '<br />' 或 '<br>'，并返回。
   is_xhtml
   是否使用 XHTML 兼容换行符。

23.ord — 返回字符的 ASCII 码值
   int ord ( string $string )
   返回字符串 string 第一个字符的 ASCII 码值。
   该函数是 chr() 的互补函数。

24.print — 输出字符串
   int print ( string $arg )
   输出 arg。
   print 实际上不是一个函数（它是一个语言结构），因此你可以不必使用圆括号来括起它的参数列表。

25.printf — 输出格式化字符串
   int printf ( string $format [, mixed $args [, mixed $... ]] )
   依据 format 格式参数产生输出。

26.rtrim — 删除字符串末端的空白字符（或者其他字符)
   string rtrim ( string $str [, string $character_mask ] )
   该函数删除 str 末端的空白字符并返回。
   不使用第二个参数，rtrim() 仅删除以下字符：
   " " (ASCII 32 (0x20))，普通空白符。
   "\t" (ASCII 9 (0x09))，制表符。
   "\n" (ASCII 10 (0x0A))，换行符。
   "\r" (ASCII 13 (0x0D))，回车符。
   "\0" (ASCII 0 (0x00))，NUL 空字节符。
   "\x0B" (ASCII 11 (0x0B))，垂直制表符。
   character_mask:
   通过指定 character_mask，可以指定想要删除的字符列表。简单地列出你想要删除的全部字符。使用 .. 格式，可以指定一个范围。

27.sha1 — 计算字符串的 sha1 散列值
   string sha1 ( string $str [, bool $raw_output = false ] )
   利用» 美国安全散列算法 1 计算字符串的 sha1 散列值。
   raw_output:
   如果可选的 raw_output 参数被设置为 TRUE，那么 sha1 摘要将以 20 字符长度的原始格式返回，否则返回值是一个 40 字符长度的十六进制数字。

28.sha1_file — 计算文件的 sha1 散列值
   string sha1_file ( string $filename [, bool $raw_output = false ] )
   利用» 美国安全散列算法 1，计算并返回由 filename 指定的文件的 sha1 散列值。该散列值是一个 40 字符长度的十六进制数字。

29.sprintf--把格式化的字符串写入变量中
   string sprintf ( string $format [, mixed $args [, mixed $... ]] )
    参数将被插入到主字符串中的百分号（%）符号处。该函数是逐步执行的。在第一个 % 符号处，插入 arg1，在第二个 % 符号处，插入 arg2，依此类推。

30.sscanf — 根据指定格式解析输入的字符
   mixed sscanf ( string $str , string $format [, mixed &$... ] )
   这个函数 sscanf() 输入类似 printf()。 sscanf() 读取字符串str 然后根据指定格式format解析, 格式的描述文档见 sprintf()。
   指定的格式字符串中的任意空白匹配输入字符串的任意空白.也就是说即使是格式字符串中的一个制表符 \t 也能匹配输入 字符串中的一个单一空格字符

31.str_replace — 子字符串替换
   mixed str_replace ( mixed $search , mixed $replace , mixed $subject [, int &$count ] )
   该函数返回一个字符串或者数组。该字符串或数组是将 subject 中全部的 search 都被 replace 替换之后的结果。
   如果 search 和 replace 为数组，那么 str_replace() 将对 subject 做二者的映射替换。如果 replace 的值的个数少于 search 的个数，多余的替换将使用空字符串来进行。如果 search 是一个数组而 replace 是一个字符串，那么 search 中每个元素的替换将始终使用这个字符串。该转换不会改变大小写。
   如果 search 和 replace 都是数组，它们的值将会被依次处理。
   search
   查找的目标值，也就是 needle。一个数组可以指定多个目标。
   replace
   search 的替换值。一个数组可以被用来指定多重替换。
   subject
   执行替换的数组或者字符串。也就是 haystack。
   如果 subject 是一个数组，替换操作将遍历整个 subject，返回值也将是一个数组。
   count
   如果被指定，它的值将被设置为替换发生的次数。
   返回值
   该函数返回替换后的数组或者字符串。

32.str_pad — 使用另一个字符串填充字符串为指定长度
   string str_pad ( string $input , int $pad_length [, string $pad_string = " " [, int $pad_type = STR_PAD_RIGHT ]] )
   该函数返回 input 被从左端、右端或者同时两端被填充到制定长度后的结果。如果可选的 pad_string 参数没有被指定，input 将被空格字符填充，否则它将被 pad_string 填充到指定长度。

33.str_repeat — 重复一个字符串
   string str_repeat ( string $input , int $multiplier )
   返回 input 重复 multiplier 次后的结果。

34.str_replace — 子字符串替换
   mixed str_replace ( mixed $search , mixed $replace , mixed $subject [, int &$count ] )
   该函数返回一个字符串或者数组。该字符串或数组是将 subject 中全部的 search 都被 replace 替换之后的结果。

35.str_split — 将字符串转换为数组
   array str_split ( string $string [, int $split_length = 1 ] )
   将一个字符串转换为数组。
   string
   输入字符串。
   split_length
   每一段的长度

36.str_word_count — 返回字符串中单词的使用情况
   mixed str_word_count ( string $string [, int $format = 0 [, string $charlist ]] )
   统计 string 中单词的数量。如果可选的参数 format 没有被指定，那么返回值是一个代表单词数量的整型数。如果指定了 format 参数，返回值将是一个数组，数组的内容则取决于 format 参数。format 的可能值和相应的输出结果如下所列。
   对于这个函数的目的来说，单词的定义是一个与区域设置相关的字符串。这个字符串可以包含字母字符，也可以包含 "'" 和 "-" 字符（但不能以这两个字符开始）。
   format:
   指定函数的返回值。当前支持的值如下：
   0 - 返回单词数量
   1 - 返回一个包含 string 中全部单词的数组
   2 - 返回关联数组。数组的键是单词在 string 中出现的数值位置，数组的值是这个单词
   返回一个数组或整型数，这取决于 format 参数的选择。

37.strstr — 查找字符串的首次出现
   string strstr ( string $haystack , mixed $needle [, bool $before_needle = false ] )
   返回 haystack 字符串从 needle 第一次出现的位置开始到 haystack 结尾的字符串。
   needle
   如果 needle 不是一个字符串，那么它将被转化为整型并且作为字符的序号来使用。
   before_needle
   若为 TRUE，strstr() 将返回 needle 在 haystack 中的位置之前的部分。

38.stripos — 查找字符串首次出现的位置（不区分大小写
   int stripos ( string $haystack , string $needle [, int $offset = 0 ] )
   返回在字符串 haystack 中 needle 首次出现的数字位置。
   与 strpos() 不同，stripos() 不区分大小写。

39.strip_tags — 从字符串中去除 HTML 和 PHP 标记
   string strip_tags ( string $str [, string $allowable_tags ] )
   该函数尝试返回给定的字符串 str 去除空字符、HTML 和 PHP 标记后的结果。
   allowable_tags
   使用可选的第二个参数指定不被去除的字符列表

40.strlen — 获取字符串长度
   int strlen ( string $string )
   返回给定的字符串 string 的长度。

41.strnatcmp — 使用自然排序算法比较字符串

42.strnatcasecmp — 使用“自然顺序”算法比较字符串（不区分大小写）

43.strpbrk — 在字符串中查找一组字符的任何一个字符
   string strpbrk ( string $haystack , string $char_list )
   strpbrk() 函数在 haystack 字符串中查找 char_list 中的字符。区分大小写
   返回一个以找到的字符开始的子字符串。如果没有找到，则返回 FALSE。

44.strpos — 查找字符串首次出现的位置
   mixed strpos ( string $haystack , mixed $needle [, int $offset = 0 ] )
   返回 needle 在 haystack 中首次出现的数字位置。

45.strrchr — 查找指定字符在字符串中的最后一次出现
   string strrchr ( string $haystack , mixed $needle )
   该函数返回 haystack 字符串中的一部分，这部分以 needle 的最后出现位置开始，直到 haystack 末尾。

46.strrev — 反转字符串

47.strtolower — 将字符串转化为小写

48.strtoupper — 将字符串转化为大写

49.strtr — 转换指定字符
   string strtr ( string $str , string $from , string $to )
   string strtr ( string $str , array $replace_pairs )
   该函数返回 str 的一个副本，并将在 from 中指定的字符转换为 to 中相应的字符。 比如， $from[$n]中每次的出现都会被替换为 $to[$n]，其中 $n 是两个参数都有效的位移(offset)。
   如果 from 与 to 长度不相等，那么多余的字符部分将被忽略。 str 的长度将会和返回的值一样。
   str
   待转换的字符串。
   from
   字符串中与将要被转换的目的字符 to 相对应的源字符。
   to
   字符串中与将要被转换的字符 from 相对应的目的字符。
   replace_pairs
   参数 replace_pairs 可以用来取代 to 和 from 参数，因为它是以 array('from' => 'to', ...) 格式出现的数组。

50.substr — 返回字符串的子串
   string substr ( string $string , int $start [, int $length ] )
   返回字符串 string 由 start 和 length 参数指定的子字符串。

51.ucwords — 将字符串中每个单词的首字母转换为大写
   这里单词的定义是紧跟在空白字符（空格符、制表符、换行符、回车符、水平线以及竖线）之后的子字符串。

52.trim — 去除字符串首尾处的空白字符（或者其他字符）
   string trim ( string $str [, string $charlist = " \t\n\r\0\x0B" ] )
   此函数返回字符串 str 去除首尾空白字符后的结果。如果不指定第二个参数，trim() 将去除这些字符：
   " " (ASCII 32 (0x20))，普通空格符。
   "\t" (ASCII 9 (0x09))，制表符。
   "\n" (ASCII 10 (0x0A))，换行符。
   "\r" (ASCII 13 (0x0D))，回车符。
   "\0" (ASCII 0 (0x00))，空字节符。
   "\x0B" (ASCII 11 (0x0B))，垂直制表符。
   charlist
   可选参数，过滤字符也可由 charlist 参数指定。一般要列出所有希望过滤的字符，也可以使用 “..” 列出一个字符范围。

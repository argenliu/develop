## shell 常用
- 输出时间
  - `date '+%F %T.%3N'`
  - `date '+%F %T.%N' | cut -b 1-23`
- 生成随机密码
  - `openssl rand -base64 6 | tr -d '\n' && echo "@TCE"`
- 字符串替换 中文逗号换成英文逗号
  - `sed -i "s/，/,/g"`
- 文件逐行读取
``` shell
while read line
do
    ($line do something...)
done < $input_file
```
- 字符串分割用 , 分割成数组
  - `array=(${str//,/ })`
- 字符串是否包含字串 is
  - `if [[ "$str" =~ "is" ]]`
- 字符串空判断
  - `if [ -z "$str" ]`
- 字符串相等判断
  - `if[ "$str1" == "$str2" ]`
  - `if[ "$str1" != "$str2" ]`
- 获取数组size
  - `size = ${#array[@]}`
- 数组访问
``` shell
for item in ${array[@]}
do
    (do something...)
done
```

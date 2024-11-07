## shell 常用
- 输出时间
  - `date '+%F %T.%N' | cut -b 1-23`
- 生成随机密码
  - `openssl rand -base64 6 | tr -d '\n' && echo "@TCE"`
- 字符串替换
  - `sed -i "s/，/,/g"`
- for 循环参考
  - 数组访问
    - ``` shell
      for item in ${array[@]}
      do
        (dosomething...)
      done
      ```

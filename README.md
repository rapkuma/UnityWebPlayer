-------------------------------------------------
배포 설정 - Github 무료는 하나만 배포 가능
Setting - Pages - master 선택 - Save

Actions 확인


-------------------------------------------------
빌드 에러
SyntaxError: Invalid or unexpected token

Unity Build Settings에서 Decompression Fallback을 체크하거나, Compression Format을 Disabled로 설정하여 빌드 후 테스트합니다. (Github 용)



https://velog.io/@fgprjs/3.-Apache-Web-Server-%EA%B5%AC%EC%B6%95-%EB%B2%95

Compression Format은 Gzip이나 Brotli 중에 하나로 한다. 이 중 어떤 설정을 선택했느냐에 따라 httpd(apache2) 설정이 바뀐다.

Decompression Fallback은 서버가 Gzip이나 Brotli의 압축을 해제할 줄 모를 때 설정하는 것인데, 브라우저에서의 로딩 시간이 많이 길어지는 관계로 가급적 설정하지 않는게 좋다.
(이 옵션을 켜놓으면 로딩하기 전에 그 어떤 리소스도 제공하지 않고 시간은 오래 걸리는 이상한 과정이 추가된다.)

DataCaching은 unityweb 데이터를 다시 받을 일 없게 캐싱해주는 브라우저 설정이다(관련 Unity 문서). 이 옵션을 켜놓으면 캐싱 후의 로딩 속도가 비약적으로 빨라지고, 서버의 부담이 매우 크게 줄어드니 설정하는 것이 좋다.

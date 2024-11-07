# 390_cham_s
Mac의 390입력기를 사용해서, karabiner-elements를 이용해 참신세벌식S를 구현하기 위해 만들었습니다.

## 참신세벌식S (S for Semoi)
참신세벌식S에 대해서는 [https://github.com/kyoungtarkkim/hangul-c3s](https://github.com/kyoungtarkkim/hangul-c3s)을 참조해 주시기를 바랍니다.

## 두 가지 파일
두 종류의 파일이 있습니다.  

390_cham_s.json은 단순히 390입력기 위에 참신세벌식S가 구동되도록 만들어 주는 파일입니다.  
karabiner-elements를 통해서 작동하는 것이므로, Mac의 390입력기를 변화시키는 것이 아닙니다!  

390_cham_s_merged.json은 조금 더 복잡한 기능을 구현하기 위해 만들었습니다.  
두 파일을 사용하기 위해 공통적으로, Mac에서 390 입력기를 먼저 추가해 주세요.

## karabiner complex modifications 설정
karabiner-elements의 complex modifications를 사용하기 위해서는 사용하고자 하는 파일을 미리 ~/.config/karabiner/assets/complex_modifications/ 디렉토리로 옮겨 놓아야 합니다.
390_chak_s.json 또는 390_cham_s_merged.json 파일을 이 폴더로 복사해주세요.

## 390_cham_s_merged.json
이 파일은 한글, 영문 변환 글자를 화면에 나타내고(hammerspoon 이용), emacs내에서는 한영 전환이 내부입력기를 변환시키게 하며,  
두벌식과 세벌식390을 동시에 사용할 수 있게끔(자신 또는 다른 사람을 위해) 해주는 역할도 포함합니다.  

이 파일이 제대로 구동되기 위해서는 몇가지 설정이 필요합니다:  
1. Mac의 설정에서 키보드 단축키 - 입력 소스 - 이전 입력 소스 선택을 F19키로 바꾸어 주세요(이 때, Karabiner를 이용하여 가령, Right Command키를 F19키로 먼저 할당하시고, 이를 이용해서 이전 소스 선택 키 세팅을 하실 수 있습니다).
2. hammerspoon을 설치해 주세요. brew install hammerspoon을 통해서 쉽게 가능합니다. ~/.hammerspoon/init.lua 파일을 만드시고, require("hs.ipc") 한줄을 적어주세요.

 ### 390_cham_s_merged.json 파일 사용법
 karabiner-elements를 이용해서 Right Command를 F19로 설정한 후, Mac에서 F19를 이용해서 입력기 변환을 한다고 가정하겠습니다.
 이 때, Right Option + Right Command 키를 이용해서 두벌식을 사용할 것인지, 세벌식390을 사용할 것인지, 참신세벌식S를 사용할 것인지 선택하실 수 있습니다.
 
 ### 두벌식의 중요성!
 보통 세벌식을 쓰시는 분은 많지 않으므로, 여러사람들이 사용하는 컴퓨터에는 두벌식이 되도록 세팅해 놓는 일은 꽤 중요한 일인 것 같습니다!

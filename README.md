# C.R.U.D 게시판 WEB Client 입니다. 
---
# 유저 요구사항 및 유저 스토리 
## 공통 스토리 (방문객 스토리, 댓글 스토리 업데이트 되어야함.)
> **권한 정리**
>> - **공통 권한: 글 보기, 댓글 작성, 댓글 수정, 댓글 삭제**
>> - **작성자 권한: 글 생성, 글 삭제, 글 수정**
>> - **방문객 권한: 공통 권한과 동일**
>
> **홈페이지 첫 진입 시**
>> - 메인 페이지로 이동되어진다.
>> - 작성자 권한을 원할 경우 우측 상단의 로그인 버튼을 클릭하여 로그인 페이지로 이동한다.
>> - 방문객일 경우 메인 페이지 스토리로 진행된다.
>
> **로그인 페이지**
>> - 계정이 존재하지 않은 유저는 로그인 폼 하단에 회원가입 버튼을 눌러 회원가입 페이지로 이동한다.
>> - 아이디를 1 번째 input에 입력한다.
>> - 비밀번호를 2 번째 input에 입력한다.
>> - 유저는 로그인 버튼을 클릭하여 입력된 아이디, 비밀번호로 로그인을 요청한다.
>> - 로그인에 실패할 경우 우측 상단에 로그인 실패 이유와 함께 로그인에 실패한다.
>> - 로그인에 성공할 경우 메인 페이지로 이동한다.
>
> **회원가입 페이지**
>> - 아이디를 1 번째 input에 입력한다.
>> - 닉네임을 2 번째 input에 입력한다.
>> - 닉네임 input옆 중복 체크 버튼을 클릭하여 닉네임 중복 체크를 한다.
>> - 이메일을 3 번째 input에 입력한다.
>> - 비밀번호를 4 번째 input에 입력한다.
>> - 입력된 비밀번호가 올바른지 확인하기 위해 5 번째 input에 입력한 비밀번호와 동일한 비밀번호를 한번 더 입력한다.
>> - form 하단에 회원가입 버튼을 클릭하여 회원가입을 요청한다.
>> - 회원가입 성공 시 로그인 페이지로 리다이렉트 된다.
>
> **메인 페이지**
>> - 유저는 1 번째 페이지로 설정된 게시판을 확인한다.
>> - 유저는 게시판의 Next 버튼을 클릭하여 2 번째 페이지로 이동한다.
>> - 유저는 11~20개의 게시글이 보이는 게시판을 확인한다.
>> - 유저는 Prev 버튼을 클릭하여 다시 1 번째 페이지로 이동하고 1~10개의 게시글이 보이는 게시판을 확인한다.
>> - 유저는 특정 게시글을 검색하기 위해 게시판 하단의 검색 기능을 이용한다.
>> - 유저는 검색 input 왼쪽에 검색 방식 select(제목, 제목 + 본문, 본문, 작성자) 에서 하나를 선택한다.
>> - 유저는 검색 input에 원하는 텍스트를 입력한 뒤 검색 버튼을 클릭하여 검색을 요청한다.
>> - 게시판에는 유저가 요청한 검색 조건의 결과 게시글들이 보여진다.
>> - 유저는 다시 전체 게시글을 보기 위해 검색 버튼 옆에 초기화 버튼 또는 빈 텍스트로 검색 요청을 한다.
>> - 유저는 게시판의 게시글을 클릭하여 해당 게시글의 상세 페이지로 이동한다.
>>
> **게시글 상세 페이지**
>> - 유저는 게시글 제목, 게시글 작성 날짜, 게시글 수정 날짜, 게시글 작성자, 게시글 본문, 게시글에 달린 댓글 리스트를 확인할 수 있다.

## 작성자 스토리
> **메인 페이지**
>> - 유저는 게시글을 작성하기 위해 게시판 하단의 게시글 작성 버튼을 클릭하여 게시글 작성 페이지로 이동한다. 
>>
>> **게시글 작성 페이지**
>>> - 유저는 제목, 본문중 하나의 input만 채우고 게시글을 작성하려 했으나 게시글 작성이 안된다.
>>> - 유저는 비어있는 제목 input과 본문 input 모두 텍스트를 입력한 뒤 게시글 작성 버튼을 클릭하여 게시글을 작성한다.
>>> - 유저는 우측 상단에 작성이 완료되었다는 메세지와 함께 메인 페이지로 이동한다.
>>
> **게시글 상세 페이지**
>> - 유저는 게시글을 수정하기 위해 게시글 본문 하단에 게시글 수정 버튼을 클릭하여 게시글 수정 페이지로 이동한다.
>>
>> **게시글 수정 페이지**
>>> - 게시글 작성 페이지와 동일하되 변경되기전의 제목과 본문 내용이 각각의 input에 표시된다.
>>> - 게시글 수정 버튼을 클릭 시 우측 상단에 수정이 완료되었다는 메시지와 함께 해당 게시글의 상세 페이지로 이동된다.
>>> - 유저는 해당 게시글의 댓글을 보기 위해 게시글 본문 하단에 댓글 리스트를 확인한다.
>>> - 댓글 하나에는 댓글 작성자, 댓글 내용, 작성 날짜, 수정 날짜를 확인할 수 있다.
>>> - 댓글 하나에는 답글이 1단계까지 존재한다.
>>> - 댓글 리스트는 게시판 명세 사항에서 검색과 한 페이지당 보여지는 게시글 수가 5개인것 외에 동일하다.
### 저번에 받은 피드백은 아직 반영되지 않았습니다.

# 요구사항

## 기본 요구사항

### 로그인, 회원가입 페이지 공통

 - [x] 로그인 및 회원가입 페이지의 이메일, 비밀번호, 비밀번호 확인 input에 필요한 유효성 검증 함수를 만들고 적용해 주세요.
- [x] 이메일 input에서 focus out 할 때, 값이 없을 경우 input에 빨강색 테두리와 아래에 “이메일을 입력해주세요.” 빨강색 에러 메세지를 보입니다.
- [x] 이메일 input에서 focus out 할 때, 이메일 형식에 맞지 않는 경우 input에 빨강색 테두리와 아래에 “잘못된 이메일 형식입니다” 빨강색 에러 메세지를 보입니다.
- [x] 비밀번호 input에서 focus out 할 때, 값이 없을 경우 아래에 “비밀번호를 입력해주세요.” 에러 메세지를 보입니다
- [x] 비밀번호 input에서 focus out 할 때, 값이 8자 미만일 경우 아래에 “비밀번호를 8자 이상 입력해주세요.” 에러 메세지를 보입니다.
- [x] input 에 빈 값이 있거나 에러 메세지가 있으면 ‘로그인’ 버튼은 비활성화 됩니다.
- [x] Input 에 유효한 값을 입력하면 ‘로그인' 버튼이 활성화 됩니다.
- [x] 활성화된 ‘로그인’ 버튼을 누르면 “/items” 로 이동합니다
const USER_DATA = [
    { email: 'codeit1@codeit.com', password: "codeit101!" },
    { email: 'codeit2@codeit.com', password: "codeit202!" },
    { email: 'codeit3@codeit.com', password: "codeit303!" },
    { email: 'codeit4@codeit.com', password: "codeit404!" },
    { email: 'codeit5@codeit.com', password: "codeit505!" },
    { email: 'codeit6@codeit.com', password: "codeit606!" },
];
로그인 페이지

- [x] 이메일과 비밀번호를 입력하고 로그인 버튼을 누른 후, 다음 조건을 참조하여 로그인 성공 여부를 alert 메시지로 출력합니다.
만약 입력한 이메일이 데이터베이스(USER_DATA)에 없거나, 이메일은 일치하지만 비밀번호가 틀린 경우, '비밀번호가 일치하지 않습니다.'라는 메시지를 alert로 표시합니다
만약 입력한 이메일이 데이터베이스에 존재하고, 비밀번호도 일치할 경우, “/items”로 이동합니다.
회원가입

- [x] 회원가입을 위해 이메일, 닉네임, 비밀번호, 비밀번호 확인을 입력한 뒤, 회원가입 버튼을 클릭하세요. 그 후에는 다음 조건에 따라 회원가입 가능 여부를 alert로 알려주세요.
입력한 이메일이 이미 데이터베이스(USER_DATA)에 존재하는 경우, '사용 중인 이메일입니다'라는 메시지를 alert로 표시합니다.
입력한 이메일이 데이터베이스(USER_DATA)에 없는 경우, 회원가입이 성공적으로 처리되었으므로 로그인 페이지(”/login”)로 이동합니다.

## 심화 요구사항

# 공통

- [x] 페이스북, 카카오톡, 디스코드, 트위터 등 SNS에서 판다마켓 랜딩 페이지(“/”) 공유 시 미리보기를 볼 수 있도록 랜딩 페이지 메타 태그를 설정합니다.
- [x] 미리보기에서 제목은 “판다마켓”, 설명은 “일상에서 모든 물건을 거래해보세요”로 설정합니다.
- [x] 주소와 이미지는 자유롭게 설정하세요.
- [ ] 로그인, 회원가입 페이지에 공통으로 사용하는 로직이 있다면, 반복하지 않고 공통된 로직을 모듈로 분리해 사용해 주세요.

### 랜딩 페이지

- [ ] 브라우저에 현재 보이는 화면의 영역(viewport) 너비를 기준으로 분기되는 반응형 디자인을 적용합니다.
PC: 1200px 이상
Tablet: 744px 이상 ~ 1199px 이하
Mobile: 375px 이상 ~ 743px 이하
375px 미만 사이즈의 디자인은 고려하지 않습니다
- [x] Tablet 사이즈로 작아질 때 최소 좌우 여백이 “판다마켓” 로고의 왼쪽에 여백 24px, “로그인” 버튼 오른쪽 여백 24px을 유지할 수 있도록 “판다마켓” 로고와 “로그인" 버튼의 간격이 가까워집니다.
- [x] Mobile 사이즈로 작아질 때 최소 좌우 여백이 “판다마켓” 로고의 왼쪽에 여백 16px, “로그인” 버튼 오른쪽 여백 16px을 유지할 수 있도록 “판다마켓” 로고와 “로그인" 버튼의 간격이 가까워집니다.
- [ ] PC, Tablet 사이즈의 이미지 크기는 고정값을 사용합니다.
- [ ] Mobile 사이즈의 이미지는 좌우 여백 32px을 제외하고 이미지 영역이 꽉 차게 구현합니다. (이때 가로가 커지는 비율에 맞춰 세로도 커져야 합니다.)
- [ ] Mobile 사이즈 너비가 커지면, “Privacy Policy”, “FAQ”, “codeit-2023”이 있는 영역과 SNS 아이콘들이 있는 영역의 사이 간격이 커집니다.

## 로그인, 회원가입 페이지 공통

- [ ] Tablet 사이즈에서 내부 디자인은 PC사이즈와 동일합니다.
- [ ] Mobile 사이즈에서 좌우 여백 16px 제외하고 내부 요소들이 너비를 모두 차지합니다.
- [ ] Mobile 사이즈에서 내부 요소들의 너비는 기기의 너비가 커지는 만큼 커지지만 400px을 넘지 않습니다.
- [x] 오류 메시지 모달을 구현합니다. 모달 내 내용은 alert 메시지와 동일합니다.
- [ ] 비밀번호 및 비밀번호 확인 입력란에 눈 모양 아이콘 클릭 시 비밀번호 표시/숨기기 토글이 가능합니다. 기본 상태는 비밀번호 숨김으로 설정합니다.


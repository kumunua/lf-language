# LF 소개

### 설명

LF 는 `.lf` 확장자를 사용하는 AOT 바이트코드 컴파일 언어예요.

LF 소스 코드는 실행 전에 LFB7 바이트코드로 컴파일되고, `lf.exe` 런타임을 통해 실행돼요.

간단한 문법, 객체 지향 구조, 네이티브 패키지, 빌드 기능 등을 제공하는 Windows x64, Linux x64 용 언어예요.

사용자 배포판은 아래와 같은 구조를 가져요.
```txt
LF/
└ lf.exe
└ boot/compiler.lfb
└ packages/
└ LICENSE.txt
```

LF 의 버전 규칙은 아래와 같아요.
```txt
YY.MM.HH.BBB
│  │  │  └─ 해당 시간대의 빌드된 횟수
│  │  └──── 빌드된 시간
│  └─────── 빌드된 달
└────────── 빌드된 연도
```

LF 의 최소 실행 구성은 아래와 같아요.
```lf
// MyLF.lf
package System

public group MyLF() {
  public function Main() {
    System.Writeln("Hello, World!");
  }
}
```

### CLI
사용법
```lf-cli
lf.exe
```

실행
```lf-cli
lf.exe <file.lf|file.lfb> [args...]
```
```lf-cli
lf.exe run <file.lf|file.lfb> [args...]
```

빌드
```lf-cli
lf.exe build <file.lf> [-o out.lfb]
```

빌드 + 실행
```lf-cli
lf.exe buildrun <file.lf> [args...]
```

### 추신

LF 의 모든 문법은 [여기서](https://lf.kumunua.kr/docs) 확인할 수 있어요.

개발자: kumunua

연락처: yongju-lee@kumunua.kr

최신 버전: `26.06.13.001`

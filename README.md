# LF 소개

### 설명

LF 는 `.lf` 확장자를 사용하는 AOT 바이트코드 컴파일 언어예요.

LF 소스 코드는 실행 전에 LFB7/BC03 바이트코드로 컴파일되고, `lf.exe` 런타임을 통해 실행돼요.

간단한 문법, 객체 지향 구조, 네이티브 패키지, 빌드 기능 등을 제공하는 Windows x64, Linux x64 용 언어예요.

사용자 배포판은 아래와 같은 구조를 가져요.
```txt
LF/
└ lf.exe
└ boot/compiler.lfb
└ packages/
  └ GraphicEngine
  └ WindowEngine
  └ Vector
  └ SoundManager
  └ DataCodec
  └ RandomKit
  └ ColorKit
  └ WebApplication
  └ Progress
```

LF 의 버전 규칙은 아래와 같아요.
```txt
YY.MM.B
│  │  └──── 빌드된 번호
│  └─────── 빌드된 달
└────────── 빌드된 연도
```
> 예) `26.07.1` -> 2026년 7월에 1번째 빌드.

LF 의 최소 실행 구성은 아래와 같아요.
```lf
// MyLF.lf
package System

public group MyLF() {
  public function Main() {
    System.Writeln("Hello, LF!");
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

빌드 및 실행
```lf-cli
lf.exe buildrun <file.lf> [args...]
```

실행 파일 빌드
```lf-cli
lf.exe build-exe <file.lf> [-o out.lfb]
```
```lf-cli
lf.exe exe <file.lf> [args...]
```
> `exe`는 `build-exe`의 약칭이고 같은 명령이에요.

### 추신

LF 의 모든 문법은 [Github Wiki](https://github.com/kumunua/lf-language/wiki/LF-Docs)나 [LF Docs](https://lf.kumunua.kr/docs)에서 확인할 수 있어요.

개발자: kumunua

연락처: yongju-lee@kumunua.kr

최신 버전: `26.07.1`

# LLDB For Debugging
## 앱 개발 시 디버깅을 위해 LLDB 명령어 사용을 통한 학습 및 테스트

### 참고 WWDC 세션 힌트
* Debugging Tips and Tricks
* Debugging with Xcode 9
* Visual Debugging with Xcode
* LLDB: Beyond "po"

### Questions
- ViewController.swift 파일의 23번째 줄에 브레이크 포인트를 설정하려면 입력해야 하는 LLDB 명령어는?
   - breakpoint set --file ViewController.swift --line 23
- `changeTextColor`라는 심볼에 브레이크 포인트를 설정하기 위해 입력해야 하는 LLDB 명령어는? 
   - breakpoint set --method changeTextColor / breakpoint set --name changeTextColor
- Debug Navigator를 통해 `titleLabel`의 `text`가 `"두 번째 뷰 컨트롤러!"`인 경우에만 작동을 일시정지하고 `titleLabel`의 `text`를 출력하는 액션을 실행하도록 설정
- 오류(Error) 혹은 익셉션(Exception)이 발생한 경우 프로세스의 동작을 멈추도록 하는 방법에 대해 알아보기
- View Controller의 뷰 위에는 사용자 눈에 보이지 않는 뷰가 있는데, 이 뷰의 오토레이아웃 제약을 확인해보기
- 디버그 모드로 실행중인 상태에서 사용자 눈에 보이지 않는 뷰의 색상을 변경해보기
- 두 번째 뷰 컨트롤러의 뷰가 화면에 표시된 상태에서, 두 번째 뷰 컨트롤러 까지의 메모리 그래프를 살펴보기
- LLDB의 `break` 명령어의 별칭인 `b` 명령어를 만들어보세요 
   - command alias b breakpoint
- LLDB의 `v`, `po`, `p` 명령어의 차이에 대해 알아봅시다
   - po : Object description, access to the full language
Evaluate an expression on the current thread.  Displays any

   - p : data formatters, access to the full language
Evaluate an expression on the current thread.  Displays any returned value with LLDB's default formatting. po        -- Evaluate an expression on the current thread.  Displays any returned value with formatting controlled by the type's author.

   - v: data formatters, iterative dynamic type resolution
Show variables for the current stack frame. Defaults to all  arguments and local variables in scope. Names of argument, local, file static and file global variables can be specified. Children of aggregate variables can be specified such as  'var->child.x'.  The -> and [] operators in 'frame variable' do not invoke operator overloads if they exist, but directly access overloads use the expression command to print the variable It is worth noting that except for overloaded operators, when  printing local variables 'expr local_var' and 'frame var  local_var' produce the same results.  However, 'frame variable' reads directly, rather than parsing and evaluating an expression, which may even involve JITing and running code in



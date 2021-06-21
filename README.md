## View Programming Guide for iOS

## Introduction

### About Windows and Views

앱에서 윈도우와 뷰를 사용해 컨텐츠를 스크린에 보여줄 수 있다. 윈도우 자체는 컨텐츠가 없지만 어플리케이션 뷰를 위한 기본적인 컨테이너를 제공한다. 뷰는 컨텐츠를 채울 윈도우의 부분을 정의한다. 예를 들어 이미지, 텍스트, 또는 다양한 조합을 보여주는 뷰를 가질 수 있다. 뷰를 사용해 다른 뷰를 조작할때도 사용할 수 도 있다.

### At a Glance

모든 앱은 적어도 한개이상의 윈도우와 뷰를 갖는다. UIKit과 다른 시스템 프레임워크가 제공하는 완성된 뷰를 사용해 컨텐츠를 보여줄 수 있다. 간단한 버튼이나 텍스트부터 복잡한 테이블뷰 피커뷰, 스크롤뷰 등을 제공한다. 이 중 원하는 뷰가 없다면 커스텀 뷰를 정의하고 이벤트 핸들링을 직접 정의 할 수 있다.

#### Views Mangage Your Application's Visual Content

뷰는 UIView 클래스의 인스턴스이자 어플리케이션 윈도우에서 직사각형 영역을 관리한다. 뷰는 컨텐츠를 그리고, 멀티터치 이벤트를 제어하며 서브뷰들을 관리한다. Core Graphics, OpenGL, UIKit과 같은 그래픽 기술을 사용해 이미지, 쉐입, 텍스트를 뷰 영역에 그리는 작업을 포함한다. 뷰는 gesture recognizer를 사용하거나 터치이벤트를 직접처리해 사각영역 내 터치 이벤트에 응답한다. 뷰 체계에서 부모 뷰는 자식 뷰의 사이즈와 위치 조정을 담당하고 이를 동적으로 수행 할 수 있다. 자식 뷰를 동적으로 수정하기에 뷰가 인터페이스 로테이션, 애니메이션과 같은 조건 변화에 즉각 대응할 수 있다.

뷰들을 인터페이스를 구성하는 구성 요소로 생각할 수 있다. 한개의 뷰가 모든 컨텐츠를 표시하는 것이 아니라 다양한 뷰를 사용해 뷰 체계를 확립할 수 있다. 뷰 체계내에 각각의 뷰는 인터페이스 영역에 특정 부분만 담당하고 특정 컨텐츠에 맞게 최적화 할 수 있다. 예를 들어 UIKit은 이미지, 텍스트 각각에 맞는 뷰를 가지고 있다.

**Relevant Chapters:** [View and Window Architecture](https://developer.apple.com/library/archive/documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/WindowsandViews/WindowsandViews.html#//apple_ref/doc/uid/TP40009503-CH2-SW1), [Views](https://developer.apple.com/library/archive/documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/CreatingViews/CreatingViews.html#//apple_ref/doc/uid/TP40009503-CH5-SW1)

#### Windows Coordinate the Display of Your Views

윈도우는 UIWindow의 인스턴스리고 앱의 전반적인 인터페이스를 다룬다. 윈도우는 뷰 체계와 상호작용 변경사항을 관리하기 위해 뷰와 함께 작동한다. 대부분 어플리케이션의 윈도우는 바뀌지 않는다. 윈도우가 만들어지고 동일하게 유지되며 뷰만 변경된다. 모든 어플리케이션은 적어도 한개 이상의 윈도우를 가지고 있다. 윈도우에서는 메인 화면에 표시되는 인터페이스를 보여준다. 외부 디스플레이가 연결되면 어플리케이션은 두번째 윈도우를 만들어 외부 디스플레이에 컨텐츠를 표시한다.

**Relevant Chapters:** [Windows](https://developer.apple.com/library/archive/documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/CreatingWindows/CreatingWindows.html#//apple_ref/doc/uid/TP40009503-CH4-SW1)

#### Animations Provide the User with Visible Feedback for Interface Changes

애니메이션은 뷰 체계의 변경사항에 대한 피드백을 사용자에게 제공한다. 시스템은 모달 뷰를 보여주고 뷰 그룹간의 전환을 위한 표준 애니메이션을 정의한다. 그러나 커스텀 애니메이션도  가능하다. 예를 들어 애니메이션을 통해 뷰의 튜명성을 변경하고 화면에서 위치 변경, 배경색 등을 변경할 수 있다.

**Relevant Chapters:** [Animations](https://developer.apple.com/library/archive/documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/AnimatingViews/AnimatingViews.html#//apple_ref/doc/uid/TP40009503-CH6-SW1)

#### The Role of Interface Builder

인터페이스 빌더를 사용해 뷰와 윈도우를 그래픽으로 구성할 수 있다. 뷰를 취합해 nib 파일에 배치 할 수 있다. 런타임에 nib 파일을 불러오면 파일안 객체들은 프로그래밍 방식으로 수정가능 실제 객체로 재구성 된다.

인터페이스 빌더는 앱의 인터페이스 작업을 매우 단순화한다. 인터페이스 빌더와 nib 파일 지원은 iOS 전반에 걸쳐서 통합되 어플리케이션 디자인에 적용하는데 큰 노력을 필요하지 않는다.

인터페이스 빌더를 위한 더많은 정보는  *[Interface Builder User Guide](https://developer.apple.com/library/archive/documentation/DeveloperTools/Conceptual/IB_UserGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40005344)* 를 참고해라. 


GTK+
====

# Tiny X
+ 메모리가 작고 성능이 떨어지는 임베디드 시스템을 위함.
+ 프레임 버퍼 위에서 동작하도록 만든 작은 x서버이다.   
+ x용 개발환경이나 응용 프로그램을 그대로 사용가능.
+ 상업용으로 사용시 별다른 제약 없음.

# MicroWindows
+ MS의 윈도우즈 API와 비슷한 API를 가짐.
+ 하드웨어, 운영체제에 의존적이 아니라 이식성이 뛰어남.
+ 하드웨어 프레임버퍼를 직접 제어하는 방식.
+ MPL(Mozlla Public License), GPL 

# Embedded QT
+ 교차 플랫폼 지원 라이브러리.
+ 프레임버퍼를 직접 제어하는 방식.
+ qmake, QT 디자이너등 툴 지원.
+ 타 GUI시스템에 비해서 용량이 큼.
+ C++
+ KDE 프로젝트 기반 위젯들로 이루어짐.

----------------------------------------------------------
<br>
<br>

# 임베디드 GUI 기술 분류
+ Full Screen형 이란 것은 하나의 응용이 전체 창을 차지하는 유형.
+ 세미 Full Screen형 PC 만큼 큰 화면을 가지고 있지는 않지만, 터치스크린 등의 사용자 입력을 받을 수 있도록 되어 있어 미세한 제어가 가능.
+ PC윈도우형은 고해상도의 편리한 사용자 입력을 가지고 있어 거의 PC와 동일한 GUI를 제공.

# 사용자 인터페이스 종류
+ CUI (Character User Interface)
+ GUI (Graphic User Interface)
+ WUI (Web User Interface)
+ Augmented GUI
+ NUI (Natural User Interface)
+ IVUI (Intelligent Visual User Interface)

# X 윈도 시스템
+ 어떤 메이커의 컴퓨터에서도 완전히 같은 외관, 사양을 가지며, 소스 수준에서의 호환성을 갖는 한편, 네트워크에 의해 각 컴퓨터가 접속 가능.
+ 공개소스화.
+ 이식성 좋음.
+ 네트워크 투명성.
+ 서버/클라이언트의 네트워크 지향 시스템.
+ X 서버 / X클라이언트 독립적.
+ TinyX, NanoX 경량 시스템 제공

# MS 윈도즈 시스템
+ 윈도 중심의 GUI
+ Windows CE 경량 시스템 제공

# GDI(Graphics Device Interface) / GDI+
+ 그래픽 카드에 대한 관련 함수들의 모임.
+ 응용프로그램과 하드웨어와 중간 계층, 하드웨어에 독립적인 인터페이스 제공.
+ GDI+는 클래스 기반 API 



# GTK+ (GIMP ToolKit)
+ GIMP를 위해 만들어짐.
+ GNU GNOME 데스크탑에서 사용하는 표준 툴킷.
+ LGPL 
+ X 위에서 돌아가기 때문에 오버헤드 있음.
+ X 윈도 시스템, BeOS등을 지원하는 멀티 플랫폼 라이브러리.
+ GTK for Frame Buffer(GtkFB)는 X윈도 시스템을 거치지 않고 커널의 프레임 버퍼에 직접접근.
+ 멀티태스킹이 쉽지 않음.
+ Glade tool

## GDK
+ GTK+ 위젯(어플리케이션)과 윈도우 시스템을 이어주는 추상적 계층을 제공.
+ Xlib(X Window에서 GUI를 개발할 수 있는 가장 기본적인 라이브러리)를 래핑.

## GTK를 이용한 창 생성 예

    #include <gtk/gtk.h>

    int main(int argc, char *argv[])

    {

        GtkWidget *window;

        gtk_init (&argc, &argv);

        window = gtk_window_new (GTK_WINDOW_TOPLEVEL);

        gtk_window_resize(GTK_WINDOW(window), 100, 100);

        gtk_widget_show (window);

        gtk_main ();

    }
















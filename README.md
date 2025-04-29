# 도서 관리 프로그램

## 📋 프로젝트 개요

도서 정보를 관리할 수 있는 콘솔 기반 프로그램을 구현합니다.

## 📁 프로젝트 구조

```
hw
    ├── model
    │   └── BookDTO.java        # 도서 정보를 담는 클래스
    ├── controller
    │   └── BookManager.java    # 도서 관리 기능 구현
    ├── view
    │   └── BookMenu.java       # 사용자 인터페이스
    └── run
        └── Application.java    # 프로그램 실행
```

## 💻 구현 클래스

### 1. BookDTO (도서 정보)

```java
public class BookDTO {
    // 필드
    private String bNo;          // 도서 번호
    private int category;     // 도서분류코드
    private String title;     // 도서 제목
    private String author;    // 도서 저자

    // 생성자
    // 1. 기본 생성자
    // 2. bNo, category, title, author를 초기화하는 생성자

    // getter/setter 메소드

    // toString() 메소드
   
   // lombok 사용해도 OK
}
```

### 2. BookManager (도서 관리)

```java
public class BookManager {
    private ArrayList<BookDTO> bookList;  // 도서 목록

    public BookManager() {
        // bookList 인스턴스 생성
    }

    public void addBook(BookDTO book) {
        // 도서 추가
    }

    public void deleteBook(int index) {
        // 전달받은 index로 도서 삭제
    }

    public int searchBook(String title) {
        // 도서명이 일치하는 객체를 찾아 해당 인덱스를 리턴
        // 도서명이 일치하는 객체가 리스트에 없으면 -1을 리턴
    }

    public void printBook(int index) {
       //인덱스 위치의 객체의 정보를 출력함
       // 인덱스 도서가 없으면 적절한 메시지 출력
    }

    public void displayAll() {
        // 도서 전체 리스트를 출력
        // 도서가 없는 경우 적절한 메시지 출력
    }
}
```

### 3. BookMenu (메뉴)

```java
public class BookMenu {
    private Scanner sc = new Scanner(System.in);
    private BookManager bm = new BookManager();

    public BookMenu() {
    }

    public void menu() {
        // 메뉴 출력
        /*
        *** 도서 관리 프로그램 ***
        1. 새 도서 추가
        2. 도서 삭제
        3. 도서 검색출력
        4. 전체 출력
        5. 끝내기
        */
        // 메뉴 번호 입력 받기
        // 잘못된 입력 처리
        // 각 메뉴에 따른 기능 실행
    }

    public BookDTO inputBook() {
        // 도서 번호 : 입력받음
        // 도서 제목 : 입력 받음
        // 도서 장르 (1:인문 / 2:자연과학 / 3:의료 / 4:기타) : 입력 받음 (숫자로)
        // 도서 저자 : 입력 받음
        // 매개변수 생성자를 이용하여 위의 초기값을 이용한 BookDTO객체 리턴
    }

    public String inputBookTitle() {
        // "도서 제목 : " 입력 받아 리턴
    }
}
```

### 4. Application (실행)

```java
public class Application {
    public static void main(String[] args) {
        // 메뉴실행
       new BookMenu().menu();
    }
}
```
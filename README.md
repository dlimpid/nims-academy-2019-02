# 제4회 국가수리과학연구소 산업수학 아카데미

## 설문조사

:heavy_exclamation_mark::heavy_exclamation_mark::heavy_exclamation_mark:[설문조사 링크](https://goo.gl/forms/j7j7RoAec5KrAtLw1):heavy_exclamation_mark::heavy_exclamation_mark::heavy_exclamation_mark:

## 보고서 템플릿

- [한/글 파일](https://github.com/dlimpid/nims-academy-2019-02/raw/master/template/%EC%A0%9C4%ED%9A%8C%20NIMS%20%EC%82%B0%EC%97%85%EC%88%98%ED%95%99%20%EC%95%84%EC%B9%B4%EB%8D%B0%EB%AF%B8%20%EA%B0%9C%EC%9D%B8%20%EB%A0%88%ED%8F%AC%ED%8A%B8.hwp)
- [Word 파일](https://github.com/dlimpid/nims-academy-2019-02/raw/master/template/%EC%A0%9C4%ED%9A%8C%20NIMS%20%EC%82%B0%EC%97%85%EC%88%98%ED%95%99%20%EC%95%84%EC%B9%B4%EB%8D%B0%EB%AF%B8%20%EA%B0%9C%EC%9D%B8%20%EB%A0%88%ED%8F%AC%ED%8A%B8.docx)

[mwna1523@nims.re.kr](mailto:mwna1523@nims.re.kr)로 2월 27일(수요일) 11시까지 보내 주세요.

## 강연 자료, 데이터 다운로드 안내

아래 목록에서 개별적으로 내려받거나 현재 상태의 전체 저장소를 [한꺼번에 내려받을](https://github.com/dlimpid/nims-academy-2019-02/archive/master.zip) 수도 있습니다(Skin cancer MNIST 데이터 제외).

### Skin cancer MNIST 데이터셋

[Kaggle 웹사이트](https://www.kaggle.com/)의 [Skin cancer MNIST](https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000) 문제 페이지에서 문제 hmnist_28_28_RGB.csv 파일을 다운로드 받으세요.

### GH 건설 데이터

[압축파일 내려받기](https://github.com/dlimpid/nims-academy-2019-02/raw/master/data/gh-data.zip)

## 전화번호 관련 안내

센터 대표 전화번호 <a href="tel:031-888-5900">031-888-5900</a>이 전화 앱, 스팸 차단 앱 등에서 다른 회사 이름으로 표시되는 경우가 있다고 합니다. 본 행사는 [국가수리과학연구소](https://www.nims.re.kr/) 산업수학혁신센터에서 진행하는 [행사](https://icim.nims.re.kr/post/event/633)입니다. 센터가 지난 2월 15일 이사를 했는데, 이전에 전화번호를 사용하던 업체의 정보가 표시되는 것으로 보입니다.

## 컴퓨터 환경 세팅

:warning: 2월 24일(일요일) 오전 9시 이전 설치하신 분 중 혹시 Python version 2로 설치되어 `print` 문에서 오류가 나시는 경우 [아래](#%EA%B8%B0%EC%A1%B4-%ED%99%98%EA%B2%BD-%EC%82%AD%EC%A0%9C-%EB%B0%A9%EB%B2%95)를 참조하셔서 환경을 삭제하신 후, 압축파일을 다시 다운받아 설치해 보세요.

:information_source: GitHub 계정이 있으시면 [Issue 페이지](https://github.com/dlimpid/nims-academy-2019-02/issues)에 질문을 올리셔도 됩니다.

:information_source: 설치 파일 용량이 크므로, 만약을 대비해 가능하면 설치 파일을 지우지 말고 남겨 두세요.

:warning: 설치할 때 가능한 한 옵션값을 바꾸지 말고 초기 상태대로 두고 설치하세요.

- "Just Me (recommended)" **선택**
- Add Anaconda to my PATH environment variable **선택하지 않기**

:warning: 아래 실행 중 2.i에서 Windows 시작 메뉴에 Anaconda3가 생성되지 않는 경우, [아래](#windows에서-anaconda-재설치시-시작-메뉴에-anaconda-prompt가-만들어지지-않는-경우)를 참고해 보세요.

:warning: 32-bit 운영체제로는 실습이 불가능합니다.

1. Anaconda 설치

    Anaconda나 Miniconda를 이미 설치한 경우에는 이전 버전으로 깔았더라도 재설치할 필요가 없이 "2. Conda 업데이트" 항목부터 하시면 됩니다.

    설치한 적이 없는 경우 [Download Anaconda Distribution](https://www.anaconda.com/download/) 페이지에서 Python 3.7 version을 받아 설치합니다.

2. Conda 업데이트

    1. 터미널(Anaconda prompt) 실행

        - Windows: 시작 -> Anaconda3 (64-bit) -> Anaconda Prompt
        - Mac: Launchpad -> 터미널

        Note: 명령줄은 OS나 환경에 따라 `(base) C:\Users\myid>`, `bash3.2$`, `MacBook:~$`, `>` 등 다양한 형식으로 보일 수 있습니다. 아래 입력을 따라할 때에는 `$` 표시 다음 부분만 입력하면 됩니다.

    2. 명령어 실행

        ```sh
        (base) $ conda update -n base conda
        ```

    3. 터미널을 닫았다가 재실행

    4. 제대로 업데이트되었는지 확인(4.6.1 이상)

        ```sh
        (base) $ conda --version
        conda 4.6.4
        ```

3. 자료 다운로드

    1. 현재 디렉터리 확인

        Anaconda가 실행되는 디렉터리를 확인합니다.

        - Windows

            기본적으로 `C:\Users\myid` 이고, 파일 탐색기에서는 `C:\사용자\myid`로 찾아가야 할 수도 있습니다. 확실하지 않은 경우 터미널을 실행하면 볼 수 있습니다.

            ```sh
            (base) C:\Users\myid>
            ```

        - Mac

            기본적으로 `/Users/myid`이고, 확실하지 않은 경우 터미널에서 `pwd` 명령어로 확인할 수 있습니다.

            ```sh
            (base) $ pwd
            /Users/myid
            ```

    2. 자료 다운로드

        다음 링크를 클릭해서 자료를 다운로드하고, 위 디렉터리에 압축을 풉니다.

        <https://github.com/dlimpid/nims-academy-2019-02/archive/master.zip>

4. 아카데미용 환경 만들기

    1. 2.i대로 터미널(Anaconda prompt) 실행

    2. 환경 만들기

        다음 명령어를 실행해서 nims-academy 이름의 환경을 만듭니다.

        ```sh
        (base) $ conda env create -f nims-academy-2019-02-master/environment.yml
        ```

        마지막에 다음과 비슷한 메시지가 나왔으면 제대로 설치된 것입니다.

        ```plain
        ...
        done
        #
        # To activate this environment, use
        #
        #     $ conda activate nims-academy
        #
        # To deactivate an active environment, use
        #
        #     $ conda deactivate
        ```

5. JupyterLab 실행

    2.i대로 터미널(Anaconda prompt)을 연 후 다음을 실행합니다.

    ```sh
    (base) $ conda activate nims-academy
    (nims-academy) $ jupyter lab
    ```

    `jupyter lab` 명령어를 칠 때 명령줄 앞에 `(nims-academy)`가 보이는지 확인해 보세요.

    Windows의 경우 다음 방법도 사용할 수 있습니다.

    1. 시작 -> Anaconda3 (64-bit) -> Anaconda Navigator
    2. **상단 "Applications on" 부분에서 "nims-academy" 선택**
    3. JupyterLab의 Launch 버튼 클릭

6. 설치 확인

    웹 브라우저에서 JupyterLab이 열리면 nims-academy-2019-02-master 디렉터리에 있는 environment-test.ipynb를 열고 Run -> Run All Cells를 실행하여

    - 모든 셀이 문제 없이 실행되는지(첫 번째나 두 번째 셀에서 오류가 나는 경우 5번의 `conda activate nims-academy`를 실행했는지 확인)
    - 그림에 한글이 잘 출력되는지(끝까지 실행되지 않고 중간에 에러가 나는 경우 notebook의 설명을 참고하여 글꼴 이름 바꾸기)

    확인해 봅니다.

---

## 참고 사항

### 기존 환경 삭제 방법

1. 터미널(Anaconda prompt) 실행

2. 다음 명령어 실행

    ```sh
    (base) $ conda env remove -n nims-academy
    ```

### 다른 디렉터리에서 JupyterLab 실행하기

기본으로 시작하는 홈 디렉터리가 아닌 다른 디렉터리나 다른 드라이브에서 JupyterLab을 실행하고 싶은 경우 디렉토리를 이동한 후 `jupyter lab`을 실행하거나, 옵션으로 지정해 줄 수 있습니다.

#### 방법 1: 디렉토리 이동

Windows와 Mac 모두 `cd` 명령어로 이동할 수 있습니다.

```sh
(nims-academy) C:\Users\myid> cd c:\path\to\go
(nims-academy) C:\path\to\go> jupyter lab
```

Windows에서 다른 드라이브로 이동할 때에는 드라이브도 바꿔 주어야 합니다.

```sh
(nims-academy) C:\Users\myid> d:
(nims-academy) D:\> cd path\to\go
(nims-academy) D:\path\to\go> jupyter lab
```

#### 방법 2: 옵션으로 지정하기

`--notebook-dir` 옵션으로 시작 디렉터리를 지정할 수 있습니다.

```sh
(nims-academy) jupyter lab --notebook-dir="C:\path\to\go"
```

### Windows에서 Anaconda 재설치시 시작 메뉴에 Anaconda prompt가 만들어지지 않는 경우

1. 제어판에서 "Python ?.?.? (Anaconda3 ...)"을 삭제
2. C:\Users\myid\Anaconda3\가 남아있으면 삭제
3. <kbd>Windows</kbd> + <kbd>r</kbd>을 누르고 "regedit" 실행
4. HKEY_CURRENT_USER\Software\Microsoft\Command Processor를 찾아가서 AutoRun, REG_EXPAND_SZ, "C:\Users\myid\Anaconda3\condabin\conda_hook.bat" 항목이 있으면 삭제
5. 재부팅한 후 재설치

그래도 안될 경우, 똑같이 하되 5번에서 재부팅한 후 [Miniconda (Python 3.7)](https://docs.conda.io/en/latest/miniconda.html)를 설치해 보세요.

# 제4회 국가수리과학연구소 산업수학 아카데미

## 컴퓨터 환경 세팅

1. Anaconda 설치

    Anaconda나 Miniconda를 이미 설치한 경우에는 이전 버전으로 깔았더라도 재설치할 필요가 없이 "2. Conda 업데이트" 항목부터 하시면 됩니다.

    설치한 적이 없는 경우 [Download Anaconda Distribution](https://www.anaconda.com/download/) 페이지에서 Python 3.7 version을 받아 설치합니다.

2. Conda 업데이트

    1. 터미널 실행

        - Windows: 시작 -> Anaconda3 (64-bit) -> Anaconda Prompt
        - Mac: Launchpad -> 터미널

        Note: 명령줄은 OS나 환경에 따라 `(base) C:\Users\myid>`, `bash3.2$`, `MacBook:~$`, `>` 등 다양한 형식으로 보일 수 있습니다. 아래 입력을 따라할 때에는 `$` 표시 다음 부분만 입력하면 됩니다.

    2. 명령어 실행

        터미널 명령줄에 `(base)`가 표시되어 있는지 확인한 후 진행합니다.

        ```sh
        (base) $ conda update conda
        (base) $ conda init
        ```

    3. 터미널을 닫았다가 재실행

    4. 제대로 업데이트되었는지 확인(4.6.1 이상)

        ```sh
        (base) $ conda --version
        conda 4.6.1
        ```

3. 자료 다운로드

    1. 현재 디렉토리 확인

        Anaconda가 실행되는 디렉토리를 확인합니다.

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

        다음 링크를 클릭해서 자료를 다운로드하고, 위 디렉토리에 압축을 풉니다.

        <https://github.com/dlimpid/nims-academy-2019-02/archive/master.zip>

4. 아카데미용 환경 만들기

    1. 터미널 실행

    2. 디렉토리 이동

        ```sh
        (base) $ cd nims-academy-2019-02
        ```

    3. 환경 만들기

        다음 명령어를 실행하면 자동으로 environment.yml 파일을 읽어서 icim-academy 환경을 만듭니다.

        ```sh
        (base) $ conda env create
        ```

        마지막에 다음과 비슷한 메시지가 나왔으면 제대로 설치된 것입니다.

        ```plain
        ...
        done
        #
        # To activate this environment, use
        #
        #     $ conda activate icim-academy
        #
        # To deactivate an active environment, use
        #
        #     $ conda deactivate
        ```

5. Jupyter 실행

    - Windows:

        1. 시작 -> Anaconda3 (64-bit) -> Anaconda Navigator
        2. **상단 "Applications on" 부분에서 "icim-academy" 선택**
        3. JupyterLab의 Launch 버튼 클릭

    - Mac(Windows도 이 방법으로도 가능):

        터미널을 연 후

        ```sh
        (base) $ conda activate icim-academy
        (icim-academy) $ jupyter lab
        ```

6. 설치 확인

    python-pandas-tutorial-nims-academy-2019-02 디렉토리에 있는 environment-test.ipynb를 열고 Run -> Run All Cells를 실행하여 모든 셀이 문제 없이 실행되는지 확인해 봅니다.

## 기타

### 기존 환경 삭제 방법

1. 터미널 실행

2. 다음 명령어 실행

    ```sh
    (base) $ conda env remove -n icim-academy
    ```

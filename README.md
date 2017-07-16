# Progress print toolkit

## Usage

기본 iterable 한 작업의 progress를 출력하기 위해서는 아래 코드를 이용한다. 이 때에는 진행 시간, 예상 시간, progress bar, 사용 메모리양이 출력된다. 

    >>> import time

    >>> l = ['n=%d'%i for i in range(100)]
    >>> for i in progress(l):
    >>>     time.sleep(1)
    >>>     continue
	
    $ |##------------------| 10.000 %, [- 0:00:11, + 0:01:30]  0.038 Gb used

만약 item이 str로 표현이 가능하다면, 각 item의 최대 출력 길이를 입력한다. 그러면 item의 str의 item_length 길이 만큼이 함께 출력된다.

    >>> for i in progress(l, item_length=5):
    >>>    continue
    
    $ |##------------------| 13.000 %, [- 0:00:14, + 0:01:27]  n=13  0.038 Gb used

출력문에 message (head)를 넣고 싶으면 progress에 head를 넣으면 된다.

    >>> for item in progress(l, head='alphabet', item_length=5):
    >>>    continue

    $ demo: |--------------------| 2.000 %, [- 0:00:03, + 0:01:38]  n=2  0.038 Gb used
    
    ...

    $ demo done. process time: 0:01:41

## Install

    pip install showprogress

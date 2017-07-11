# Progress print toolkit

## Usage

기본 iterable 한 작업의 progress를 출력하기 위해서는 아래 코드를 이용한다. 이 때에는 진행 시간, 예상 시간, progress bar, 사용 메모리양이 출력된다. 

    from showprogress import progress
	
    l = ['a', 'b', 'c', 'd']
    for item in progress(l):
        continue

만약 item이 str로 표현이 가능하다면, 각 item의 최대 출력 길이를 입력한다. 그러면 item의 str의 item_length 길이 만큼이 함께 출력된다.

    for item in progress(l, item_length=5):
        continue


## Install

    pip install showprogress

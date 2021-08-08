# 혼공머신(chapter.2)

날짜: 2021년 8월 8일

- **numpy**
    - seed : 난수 생성
    - arange : 일정한 간격의 정수 또는 실수 배열을 만든다

        ```python
        print(np.arange(3))
        >>> [0,1,2]

        print(np.arange(1,3,0.2))
        >>> [1,1.2,....2.6,2.8]
        ```

    - shuffle : 주어진 배열을  랜덤하게 섞는다.

    ```python
    arr=np.array([[1,2],[3,4],[5,6])
    np.random.shuffle(arr)
    print(arr)
    >>> [[3 4]
         [5 6]
         [1 2]]
    ```

    - column_stack() : 전달받은 리스트를 일렬로 세운 다음 차례대로 나란히 연결

    ```python
    np.column_stack(([1,2,3],[4,5,6]))
    >>> array([[1,4],
               [2,5],
               [3,6]])
    ```

- **train_test_split()**
    - rnadom_state=42 : 이걸 하는 이유는 결과가 같게 하기 위해서이다. 
    (다른사람과 나의 결과는 무작위로 달라질 수 있는데 이걸 통해서 같게 만들 수 있다.)
    - stratify=test : 이건 데이터가 적어 무작위로 나누어졌을 때, 한쪽으로 치우쳐 있는 것을 방지 할 수 있다. 저렇게 하면 test의 비율을 보고 알아서 맞게 나눠준다.

    ![%E1%84%92%E1%85%A9%E1%86%AB%E1%84%80%E1%85%A9%E1%86%BC%E1%84%86%E1%85%A5%E1%84%89%E1%85%B5%E1%86%AB(chapter%202)%200a528fe9d98f41e6afb30b90868050e2/Untitled.png](%E1%84%92%E1%85%A9%E1%86%AB%E1%84%80%E1%85%A9%E1%86%BC%E1%84%86%E1%85%A5%E1%84%89%E1%85%B5%E1%86%AB(chapter%202)%200a528fe9d98f41e6afb30b90868050e2/Untitled.png)

- 데이터 전처리(표준점수)
    - 각 데이터가 원점에서 몇 표준편차만큼 떨어져 있는지를 나타내는 값입니다.
    (평균을 빼주고,  표준편차를 나누어 주면 되는 것입니다.)

    ```python
    mean=np.mean(train_input,axis=0)
    std=np.std(train_input,axis=0)

    train_scaled=(train_input - mean) / std
    ```

    ![%E1%84%92%E1%85%A9%E1%86%AB%E1%84%80%E1%85%A9%E1%86%BC%E1%84%86%E1%85%A5%E1%84%89%E1%85%B5%E1%86%AB(chapter%202)%200a528fe9d98f41e6afb30b90868050e2/Untitled%201.png](%E1%84%92%E1%85%A9%E1%86%AB%E1%84%80%E1%85%A9%E1%86%BC%E1%84%86%E1%85%A5%E1%84%89%E1%85%B5%E1%86%AB(chapter%202)%200a528fe9d98f41e6afb30b90868050e2/Untitled%201.png)
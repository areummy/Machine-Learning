# Scikit-learn

- 머신러닝 패키지 이며 2차원 리스트가 필요함 > zip()함수를 이용하여 2차원 리스트 생성
- zip()함수는 나열된 리스트에서 원소를 하나씩 꺼내주는 일을 한다.

```python
data=[[l,w] for l,w in zip(length,weight)]
```

## K-최근접 이웃 알고리즘

- 가장 간단한 머신러닝 알고리즘 중 하나로  어떤 규칙을 찾기 보다는 인접한 샘플을 기반으로 예측을 수행한다. (단, 데이터가 많을 경우 에측하기가 어려움>직선거리  계산이 어렵기 때문에)
- KNeighborsClassifier()

    ```python
    from sklearn.neighbors import KNeighborsClassifier
    ```

[](http://localhost:8888/notebooks/Documents/GitHub/Machine%20Learning/Chapter.01/1_3_%EB%A7%88%EC%BC%93%EA%B3%BC_%EB%A8%B8%EC%8B%A0%EB%9F%AC%EB%8B%9D.ipynb)

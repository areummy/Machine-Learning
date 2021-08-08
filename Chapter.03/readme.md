# 혼공머신(capter.03)

날짜: 2021년 8월 8일

- **03-1_k-최근접이웃회귀**
    - 가까운 것들의 평균으로 예측한다.
    - **결정계수 : 분류에서는 정확도, 회귀에서는 결정계수 또는 R제곱**

- **과대적합  VS 과소적합**
    - 훈련세트와 테스트세트를 비교했을 때, 훈련세트가 너무 높으면 과대적합 !
    반대이거나, 두 점수가 너무  낮으면 과소적합!
    - **과대적합일  경우**, 덜 복잡하게(k-최근접이웃일 경우 k값을 늘림)
    - **과소적합일 경우**, 더 복잡하게 (k-최근접이웃일 경우 k값을 줄임)
- **MAE(mean absolute error)**
    - 타깃과 예측의 절댓값 오차를 평균하여 반환

    ```python
    from  sklearn.metrics import mean_absolute_error
    test_prediction=knr.predict(test_input)
    mae=mean_absolute_error(test_target,test_prediction)
    mae
    >>> 19.157142857142862
     #위 값은 예측이  평균적으로 19g정도 다르다는 것
    ```

- **reshape**
    - 배열의 크기를 지정할 수 있다.
    - 아래 -1을 넣은 이유는 데이터의 모든 행들에 적용하겠다는 의미이다.

    ```python
    train_input=train_input.reshape(-1,1)
    test_input=test_input.reshape(-1,1)

    # 이런식으로 2차원 배열로 바뀜 !!
    >>>array([[19.6],
           [22. ],
           [18.7],
           [17.4],
           [36. ],
           [25. ],
           [40. ],
           [39. ])
    ```
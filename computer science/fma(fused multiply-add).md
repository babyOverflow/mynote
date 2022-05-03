fma는 부동소수점 곱하기와 더하기를 한번에 수행한다. `fma(a, b, c) == a + (b * c)` fma를 사용하지 않는다면 `b * c` 에서 반올림을 하고 `a`와  더하는 과정에서 다시 반올림을 한다. fma를 사용하면 마지막에 한번 반올림을 수행함으로 적은 비용으로 정확도 높은 연산을 할 수 있다.

[Multiply–accumulate operation - Wikipedia](https://en.wikipedia.org/wiki/Multiply%E2%80%93accumulate_operation#Fused_multiply%E2%80%93add)
[Accurate Differences of Products with Kahan's Algorithm (pharr.org)](https://pharr.org/matt/blog/2019/11/03/difference-of-floats)

---
메모 2022 02 12
pbrt v4의 코드를 보다가 std::fma 함수를 봤다. 이전 버전에서는 내적을 할 때 `v1*u1 + v2*u2`  로 하던 것을 fma 함수를 사용하고 있어서 무슨 내용인지 찾아봤다.

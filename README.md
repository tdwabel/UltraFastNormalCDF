# High-Performance Standard Normal CDF Implementation

A high-speed, high-precision implementation of the standard normal cumulative distribution function (CDF), optimized for both accuracy and throughput.

---

## ✨ Key Features
- **Ultra-fast**: Over 800x faster than mpmath.ncdf
- **High precision**: Maximum absolute error under 1e-5
- **Numerically stable**: Symmetric evaluation eliminates cancellation errors
- **Production-ready**: Lightweight, no heavy dependencies

---

## 📊 Benchmark Results

### Accuracy vs mpmath (41 points, step 0.25 from 0 to -10)
![Accuracy Benchmark](https://p26-flow-imagex-sign.byteimg.com/tos-cn-i-a9rns2rl98/771f257cfed34155be86f3fc21dbeccc.png)

### Performance Comparison
![Performance Benchmark](https://p26-flow-imagex-sign.byteimg.com/tos-cn-i-a9rns2rl98/12f241d4975e46f58ee99f2d9f575f91.png)

---

## 📈 Error Characteristics
- Max absolute error: ~1e-5
- Tail error decays to machine precision
- Symmetric calculation for numerical stability

---

## 🚀 Usage Example
```python
from high_precision_cdf import norm_cdf

print(norm_cdf(0.0))   # 0.5
print(norm_cdf(-1.0))  # ~0.158655
print(norm_cdf(2.0))   # ~0.977250

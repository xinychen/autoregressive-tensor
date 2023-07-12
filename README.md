# Low-Rank Autoregressive Tensor Completion

**Low-rank autoregressive tensor completion for spatiotemporal traffic data imputation**. (IEEE TITS'22)

```bibtex
@article{chen2022low,
  title={Low-rank autoregressive tensor completion for spatiotemporal traffic data imputation},
  author={Chen, Xinyu and Lei, Mengying and Saunier, Nicolas and Sun, Lijun},
  journal={IEEE Transactions on Intelligent Transportation Systems},
  volume={23},
  number={8},
  pages={12301--12310},
  year={2022},
  publisher={IEEE}
}
```

<br>

## Features

- **Highlights**
  - Present a missing data imputation approach that utilizes the day dimension of traffic data.
  - Build a tensor completion task through truncated nuclear norm minimization.
  - Consider univariate autoregressive process along the temporal dimension to characterize the time series trends.

- **New features in the repo**
  - Use conjugate gradient to solve the linear equations, intead of least squares in the [transdim](https://github.com/xinychen/transdim) repo.
  - Include both `CPU` (with `import numpy as np`) and `GPU` (with `import cupy as np`) implementation.

<br>

## Datasets

- [**Seattle freeway traffic speed dataset**](https://github.com/zhiyongc/Seattle-Loop-Data): This dataset contains freeway traffic speed from 323 loop detectors on the freeway network with a 5-minute time resolution (i.e., 288 time steps per day) over the first four weeks of January, 2015 in Seattle, USA. The processed data is of size 323-by-8,064 in the form of multivariate time series matrix. Alternatively, introducing the day dimension would lead to a tensor data of size 323-by-288-by-28. [[`tensor.npz`](https://github.com/xinychen/autoregressive-tensor/blob/main/tensor.npz)]
- [**Portland highway traffic volume dataset**](https://portal.its.pdx.edu/home): This dataset is collected from the highway network of the Portland-Vancouver Metropolitan region, which contains traffic volume from 1,156 loop detectors with a 15-minute time resolution (i.e., 96 time steps per day) in January, 2021. The processed data is of size 1,156-by-2,976 in the form of multivariate time series matrix. Alternatively, introducing the day dimension would lead to a tensor data of size 1,156-by-96-by-31. [[`volume.npy`](https://github.com/xinychen/autoregressive-tensor/blob/main/volume.npy)]

<br>



## Supported by

<a href="https://ivado.ca/en">
<img align="middle" src="https://github.com/xinychen/tracebase/blob/main/graphics/ivado_logo.jpeg" alt="drawing" height="70" hspace="50">
</a>
<a href="https://www.cirrelt.ca/">
<img align="middle" src="https://github.com/xinychen/tracebase/blob/main/graphics/cirrelt_logo.png" alt="drawing" height="50">
</a>

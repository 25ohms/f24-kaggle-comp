- Used Multi-class Logarithmic Loss:

$$
MLC = -\frac{1}{n} \sum^N_{i=1} \sum^M_{j=1} y_{ij} \log(p_ij)
$$

where $y_{ij}$ is an indicator to whether sample $i$ belongs to class $j$, and $p_{ij}$ is the probability predicted by the model that sample $i$ belongs to class $j$.

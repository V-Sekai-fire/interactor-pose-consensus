# interactor-pose-consensus

A parametric referee that fits a human body model to keypoints and judges whether a body could hold that pose.

## What it is for

A generated image is checked against the pose that conditioned it. The referee fits the body model to the keypoints read back from the image and rejects a pose the model cannot reach, even when every estimator agrees on it; finger chains whose error grows joint by joint are marked untrusted. Beside it are a soft silhouette and a soft depth renderer for the same fit, a contour tracer for silhouette masks, and a licence gate for the models a corpus may use.

## Run it

Each module runs as a script and prints its own controls:

```sh
python python/soma_referee.py
python python/test_backend_licenses.py
```

## Licence

Apache-2.0 OR MIT, as the SPDX headers state.

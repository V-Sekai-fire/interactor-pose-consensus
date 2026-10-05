# interactor-pose-consensus

A parametric referee that judges the residual of a human body-model fit to keypoints, and whether a body could hold that pose.

## What it is for

A generated image is checked against the pose that conditioned it. The body model is fitted elsewhere to the keypoints read back from the image; the referee judges that fit's residual region by region and rejects a pose the model cannot reach, even when every estimator agrees on it; finger chains whose error grows joint by joint are marked untrusted. Beside it are a soft silhouette and a soft depth renderer for the same fit, a contour tracer for silhouette masks, and a licence gate for the models a corpus may use.

## Run it

Each module runs as a script and prints its own controls. The scripts need `numpy` and `torch`:

```sh
python python/soma_referee.py
python python/test_backend_licenses.py
```

## Licence

Only the two test scripts state a licence, Apache-2.0 OR MIT, in their SPDX headers. The other modules and the repository carry none.

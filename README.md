# computefence-action

Run [ComputeFence](https://github.com/Francisco-Booth/ComputeFence) pre-flight checks before your GPU training job to catch configuration mistakes before billing starts.

## Usage

Add this to your GitHub Actions workflow:

```yaml
steps:
  - uses: Francisco-Booth/computefence-action@v1
```

## Options

```yaml
- uses: Francisco-Booth/computefence-action@v1
  with:
    output-dir: ./checkpoints   # optional: check checkpoint path persistence
    dataset: ./data/train.csv   # optional: run dataset integrity checks
```

## Pod Startup Script

Not using GitHub Actions? Use the [on-start.sh gist](https://gist.github.com/Francisco-Booth/75b6f8b29defd095dd2cbb5e4bfc5a45) to add ComputeFence to your RunPod or Vast.ai pod startup command directly.

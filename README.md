# Tilt Kustomize Example

This is an example of how to use kustomize with Tilt. It really couldn't be simpler!

1. Have a directory with a `kustomization.yaml` file in it. In this case we have a directory that contains YAML for a wordpress install
2. Use the `kustomize` function in your Tiltfile to use `kustomize` to build the realized YAML.

```python
yaml = kustomize('./wordpress')
```

3. Apply that YAML to your cluster with `k8s_yaml`!

```python
k8s_yaml(yaml)
```

4. `tilt up`!

This wordpress example was taken from the [kustomize examples directory](https://github.com/kubernetes-sigs/kustomize/tree/master/examples/wordpress).
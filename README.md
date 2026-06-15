# locust-configs

Per-user `kai` CLI configs for the **production** (locust) KAI cluster
(control plane: node3, `https://10.0.0.3:6443`).

This is the production counterpart to the testbed `brachiolab-configs` repo —
kept separate so testbed and production user configs don't collide.

## Layout

    <namespace>/<username>.yaml

e.g. `brachiolab/exwong.yaml`. Each file is the config `kai setup` fetches for
that user (namespace, default queue, role, kubeconfig path). It contains **no
secrets** — kubeconfigs/tokens are delivered separately.

## Adding a user

A lab manager runs `kai add-user --name <user> --role <role>`, which pushes the
generated config here automatically (configs repo = this repo).

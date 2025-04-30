
# 🖥️ ASIOS™ Userspace

High-level tools, utilities, and libraries running atop the ASIOS™ kernel for AI orchestration, telemetry, tuning, and management.

---

## 🚀 Included Tools

| Tool                    | Description                                                         |
|-------------------------|---------------------------------------------------------------------|
| **`asios-cli`**         | CLI to manage ASIOS services, kernels, and profiles                 |
| **`asios-agent`**       | Telemetry agent for runtime monitoring and backend forwarding       |
| **`asios-gpu-manager`** | GPU partitioning (MIG), NVLink, RDMA configuration                  |
| **`asios-memory-tuner`**| User-space hugepage pools & NUMA memory balancing                   |
| **`asios-autotune`**    | Automated AI workload profiler and kernel parameter optimizer       |

**Libraries**  
- `libasios-utils` — Common utilities  
- `libasios-telemetry` — SDK for custom telemetry integrations  

---

## 📋 Prerequisites

Ubuntu 24.04 LTS (x86_64 or ARM64):

```bash
sudo apt update
sudo apt install -y git python3-pip build-essential libssl-dev
```

A running ASIOS™ kernel from [asi-os/asios-core].

---

## 🛠️ Build & Install

```bash
git clone https://github.com/asi-os/asios-userspace.git
cd asios-userspace
make -j$(nproc)
sudo make install
```

Verify installation:

```bash
which asios-cli
asios-cli --help
```

> Some tools require `sudo` (e.g. `asios-gpu-manager`).

---

## 📖 Documentation & Guides

See the ASIOS™ docs repository: https://github.com/asi-os/asios-docs  
Key files: `ARCHITECTURE.md`, `ROADMAP.md`, `CHANGELOG.md`, `ADR/`

---

## ⚖️ Contribution

- Sign the [ICLA](../asios-legal/ICLA.md).  
- Add DCO `Signed-off-by:` to every commit per [DCO](../asios-legal/DCO.md).

---

## 🤝 Support

- **Issues & PRs:** `asi-os/asios-userspace/issues`  
- **Discord:** https://discord.gg/rWuU7cWU4E  
- **Governance questions:** governance@karlex.ai  

© 2025 KarLex AI, Inc. — see [Legal Portal](https://asios.ai/legal)

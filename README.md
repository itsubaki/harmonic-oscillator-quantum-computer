# Quantum harmonic oscillator simulator for quantum computation

A demo built with HTML, CSS, and JavaScript that implements CNOT through the free time evolution of a quantum harmonic oscillator.
It uses the encoding and time evolution described in Nielsen & Chuang, *Quantum Computation and Quantum Information*, §7.3.

```text
|00⟩_L = |0⟩
|01⟩_L = |2⟩
|10⟩_L = (|4⟩+|1⟩)/√2
|11⟩_L = (|4⟩−|1⟩)/√2
```

$$
c_n(\tau) = c_n(0)\exp(-in\tau), \qquad \tau = \omega t
$$

At τ = π, the result matches the logical CNOT output. Mean energy includes the zero-point energy, while time evolution omits the global phase exp(−iτ/2).
Fidelity measures agreement with the ideal CNOT output for the selected input; it is not a general gate fidelity.
Loss, environmental effects, and physical state-preparation or measurement hardware are not modeled.

## GitHub Pages

The site is entirely static and needs no build step. Only the contents of `public/` are deployed.

1. In the repository's **Settings → Pages → Build and deployment**, set **Source** to **GitHub Actions**.
2. Push `.github/workflows/pages.yml` to `main`. The workflow runs automatically when `public/` or the workflow changes on `main`, and can also be started manually from **Actions → Deploy to GitHub Pages → Run workflow**.
3. After deployment succeeds, open <https://itsubaki.github.io/harmonic-oscillator-quantum-computer/>.

For local preview, run `make run` and open <http://127.0.0.1:3000/>.

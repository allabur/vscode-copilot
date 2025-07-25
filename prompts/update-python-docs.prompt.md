---
mode: "agent"
tools: ["codebase"]
description: "Rewrite Python docstrings to English NumPy style and inject coherent Step comments"
---

# Prompt name  `update-python-docs`

## Goal  🚀

Rewrite **all** documentation in the supplied Python context (`${file}` or `${selection}`) so that it is:

1. Written in **English**.
2. Formatted with the official **NumPy docstring standard** (Summary, Extended Summary, Parameters, Returns, Raises, Examples, Notes).
3. Complete: every parameter & return value documented with **name : type — description**.
4. All functions have complete type annotations: `parameter: TypeAnnotation = default_value`.
5. Type hints follow modern Python standards and match implementation
6. Synchronized with the current implementation (no stale or misleading info).
7. Line‑wrapped to ≤ 72 characters inside docstrings.

## Workflow  🔧

1. **Load context**: use `#file` if present, otherwise ask the user to select the file.
2. **Infer and add complete types** (PEP‑484 style) from code analysis and context.
3. **Add missing type annotations** for all parameters and return values.
4. **Validate type consistency** between annotations, docstrings, and implementation.
5. **Replace or create** docstrings:
   - First line in _imperative mood_ (e.g., "Compute mean value.").
   - Follow the exact section order mandated by _numpydoc_.
6. **Insert numbered comments** for complex logic blocks:
   ```python
   # Step 1: normalize input
   # Step 2: run optimization
   ```
7. **Validate** with `pydocstyle --convention=numpy`; if errors remain, fix and re‑run.
8. **Output** only the _complete updated file_ wrapped in triple‑back‑tick python fences—no extra commentary.

## Type Annotation Requirements ⚡

- Every function parameter must have a type annotation
- Every function must have a return type annotation
- **Use modern typing syntax (Python 3.9+)**:
  - `list[str]` instead of `List[str]`
  - `dict[str, int]` instead of `Dict[str, int]`
  - `str | None` instead of `Optional[str]`
  - `str | int | bool` instead of `Union[str, int, bool]`
- **Only import from typing when necessary**: `Literal`, `Callable`, `TypeVar`, `Protocol`
- Match pandas/numpy types: `pd.DataFrame`, `pd.Series`, `np.ndarray`
- Ensure type consistency between function signature, docstring, and implementation

## Acceptance criteria  ✅

- Zero `pydocstyle` errors or warnings.
- All functions have complete type annotations.
- Type annotations match implementation and usage.
- No `TODO`/`FIXME` tokens left.
- Unit tests (if any) still pass; logic unchanged.

---

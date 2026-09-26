# Lab 11 — Auto Report

> File này **tự sinh** bởi `scripts/grade.py`. **Không** viết / sửa tay.

- Generated (UTC): `2026-09-26T08:47:37.710077+00:00`
- Framework: `google-adk`
- Technical failure: **False**

## Packaging

| File | Status |
|------|--------|
| results.json | OK |
| attack_results.json | OK |
| audit_log.json | OK |
| metrics.json | OK |

## Schema (`results.json`)

- Valid: **True**
- Error: `None`

## Defense snapshot (từ `results.json`)

- Safe queries blocked: `0/5`
- Attack queries blocked: `7/7`
- Edge cases blocked: `3/3`
- Rate limit blocked/sent: `3/8`

## Red Team snapshot (từ `attack_results.json`)

- Provider / model: `openai` / `gpt-4o-mini`
- Unsafe leaks (Red): `5/5`
- Guards leaks (Red Advance): `0/5`

## Public tests

- Return code: `0`
- Technical failure: `False`

```text
 google.cloud.aiplatform.v1beta1.schema.predict.params_v1beta1.
    warnings.warn(message, FutureWarning)

tests/public/test_lab_contracts.py::test_detect_injection_basic
  /Users/chung140204/K4-L3-DAY11-NgoDucChung-2A202602985-Guardrails-HITL-Responsible-AI/.venv/lib/python3.9/site-packages/google/api_core/_python_version_support.py:242: FutureWarning: You are using a non-supported Python version (3.9.6). Google will not post any further updates to google.cloud.aiplatform.v1beta1.schema.predict.prediction_v1beta1 supporting this Python version. Please upgrade to the latest Python version, or at least Python 3.10, and then update google.cloud.aiplatform.v1beta1.schema.predict.prediction_v1beta1.
    warnings.warn(message, FutureWarning)

tests/public/test_lab_contracts.py::test_detect_injection_basic
  /Users/chung140204/K4-L3-DAY11-NgoDucChung-2A202602985-Guardrails-HITL-Responsible-AI/.venv/lib/python3.9/site-packages/google/api_core/_python_version_support.py:242: FutureWarning: You are using a non-supported Python version (3.9.6). Google will not post any further updates to google.cloud.aiplatform.v1beta1.schema.trainingjob.definition_v1beta1 supporting this Python version. Please upgrade to the latest Python version, or at least Python 3.10, and then update google.cloud.aiplatform.v1beta1.schema.trainingjob.definition_v1beta1.
    warnings.warn(message, FutureWarning)

-- Docs: https://docs.pytest.org/en/stable/how-to/capture-warnings.html
10 passed, 15 warnings in 1.51s
```

## Notes

- Artifact chấm chính: `outputs/results.json` + `outputs/attack_results.json`.
- Bonus B1/B2 do grader replay quyết định — JSON chỉ là bằng chứng.
- Không nộp `report/*.md` viết tay; dùng file này nếu cần xem tóm tắt.

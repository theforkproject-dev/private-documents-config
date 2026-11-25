# Private Documents measured configuration

Single-H200 Gemma4-31B BF16 document conversion/OCR baseline. Owned document-only gateway in the same confidential deployment; no hosted inference fallback. Parser remains a separate networkless container. Document/model networks are closed. No public signup or general inference API.

Public artifacts contain only runtime pins and a high-entropy credential's SHA256 verifier, not credentials or documents. The implementation and corresponding-source access are held in the authorized private source repository. Platform measurement workflow performs publication, not application builds; application binaries were built and tested in a dedicated attested Bunker.

Deployment is not accepted until fresh authentic CPU/GPU evidence, key-bound transport, native Perimeter access and actual OCR/negative tests pass. HTTPS reachability alone is not attestation. No private documents authorized yet.

Updates must STOP the one existing H200 instance, wait until stopped, then deploy the new tag. Never use default single-GPU blue/green updates, which would borrow a second GPU. Successful accepted service is retained; temporary workshops have a separate lifecycle.

## v0.0.2 qualification correction

The initial32CPU/128GiB/two-model-disk layout was API-valid but absent from published platform endorsements; fresh attestation failed closed. This release selects16CPU/128GiB/oneGPU/six total disks, matching the published medium_3d_new shape. A dedicated1GB compatibility disk is attached solely to match that endorsed hardware layout. It remains locked, unformatted and unmounted in every application container. It stores neither code nor document content, and grants no worker/admin authority. This is actual hardware-layout selection, not a measurement override; fresh verification still must pass.

Temporary Gemma startup-log health diagnostics are enabled for PUBLIC/SYNTHETIC qualification only. No private inputs until these are removed and acceptance passes. Model, image, BF16 precision and model arguments remain unchanged.

## v0.0.3 readiness qualification

v0.0.2 native Perimeter verified fresh V3 attestation and reached the shim over its key-bound transport. The layout correction worked. Gemma readiness still failed after85s despite the declared30m start_period. Only sidecar connection-refused logs were captured, not a proven child crash. v0.0.3 preserves the same real HTTP health criterion but waits inside a bounded30-minute health probe; it never returns healthy before the real endpoint succeeds. Startup stdout is unbuffered for this public-only qualification. No model/parser/image/security downgrade.

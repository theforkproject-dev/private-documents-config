# Private Documents measured configuration

Single-H200 Gemma4-31B BF16 document conversion/OCR baseline. Owned document-only gateway in the same confidential deployment; no hosted inference fallback. Parser remains a separate networkless container. Document/model networks are closed. No public signup or general inference API.

Public artifacts contain only runtime pins and a high-entropy credential's SHA256 verifier, not credentials or documents. The implementation and corresponding-source access are held in the authorized private source repository. Platform measurement workflow performs publication, not application builds; application binaries were built and tested in a dedicated attested Bunker.

Deployment is not accepted until fresh authentic CPU/GPU evidence, key-bound transport, native Perimeter access and actual OCR/negative tests pass. HTTPS reachability alone is not attestation. No private documents authorized yet.

Updates must STOP the one existing H200 instance, wait until stopped, then deploy the new tag. Never use default single-GPU blue/green updates, which would borrow a second GPU. Successful accepted service is retained; temporary workshops have a separate lifecycle.

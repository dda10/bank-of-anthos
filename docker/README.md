# Own Dockerfiles (rebuilt from scratch — do NOT use upstream).
#
# The container-fundamentals pillar: multi-stage, non-root, pinned base
# digests. One Dockerfile per service, named `<service>.Dockerfile`.
#
# Phase A work items:
#   [ ] frontend.Dockerfile            (src/frontend — Python)
#   [ ] accounts.Dockerfile            (src/accounts — Java/Spring Boot)
#   [ ] contacts.Dockerfile            (src/accounts/contacts — Python)
#   [ ] userservice.Dockerfile         (src/accounts/userservice — Java)
#   [ ] ledgerwriter.Dockerfile        (src/ledger/ledgerwriter — Java)
#   [ ] balancereader.Dockerfile       (src/ledger/balancereader — Java)
#   [ ] transactionhistory.Dockerfile  (src/ledger/transactionhistory — Java)
#   [ ] loadgenerator.Dockerfile       (src/loadgenerator — Python/Locust)
#
# Rules per service:
#   - multi-stage: build stage → slim runtime stage
#   - run as non-root UID (create user, drop privileges)
#   - pin base images to digest, not tag
#   - HEALTHCHECK / non-privileged ports only

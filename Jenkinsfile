# Tenant pipeline stub — the ENTIRE CI/CD logic lives in platform-ci.
# This file must never grow CI logic; if onboarding needs more than this,
# the shared-library boundary is wrong.

@Library('platform-ci') _

bankPipeline(
  services: [
    'frontend',
    'accounts',
    'contacts',
    'userservice',
    'ledgerwriter',
    'balancereader',
    'transactionhistory',
    'loadgenerator',
  ]
)

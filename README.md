# Firefox Advanced Settings

Firefox advanced settings for increased privacy and security.

## Configure DNS over HTTPS

    // Use DoH without fallback to insecure DNS
    network.trr.mode = 3

    network.trr.uri = https://dns.paesa.es/dns-query
    network.trr.useGET = true

## Enable HTTPS-Only Mode

    dom.security.https_only_mode = true
    dom.security.https_only_mode_ever_enabled = true

## Enable HTTP3/QUIC

    network.http.http3.enabled = true

## SSL/TLS

    // Disable TLS 1.0 and TLS 1.1
    security.tls.version.min = 3
    
    // Enable TLS Delegated Credentials
    security.tls.enable_delegated_credentials = true

    // Disable Weak Ciphersuites
    security.ssl3.ecdhe_ecdsa_aes_128_sha = false
    security.ssl3.ecdhe_ecdsa_aes_256_sha = false
    security.ssl3.dhe_rsa_aes_128_sha = false
    security.ssl3.dhe_rsa_aes_256_sha = false
    security.ssl3.ecdhe_rsa_aes_128_sha = false
    security.ssl3.ecdhe_rsa_aes_256_sha = false
    security.ssl3.rsa_aes_128_gcm_sha256 = false
    security.ssl3.rsa_aes_128_sha = false
    security.ssl3.rsa_aes_256_gcm_sha384 = false
    security.ssl3.rsa_aes_256_sha = false
    security.ssl3.rsa_des_ede3_sha = false

    // Disable OCSP
    security.OCSP.enabled = 0
    security.OCSP.require = false

    // Enforce CRLite Revocation Checks
    security.pki.crlite_mode = 2

    // Enable Encrypted Client Hello (ECH/ESNI)
    network.dns.echconfig.enabled = true
    network.dns.use_https_rr_as_altsvc = true

## Sandbox

    // Enable Site Isolation Sandboxing
    fission.autostart = true

    // Windows only process hardening
    security.sandbox.content.win32k-disable = true
    security.sandbox.gmp.win32k-disable = true

## Resist Fingerprinting

    privacy.resistFingerprinting = true
    privacy.spoof_english = 2

## Reject Third-Party Cookies

    network.cookie.cookieBehavior = 1

## Tracking Protection

    privacy.trackingprotection.enabled = true
    privacy.trackingprotection.fingerprinting.enabled = true
    privacy.trackingprotection.cryptomining.enabled = true
    privacy.trackingprotection.socialtracking.enabled = true
    privacy.socialtracking.block_cookies.enabled = true
    privacy.firstparty.isolate = true
    privacy.donottrackheader.enabled = true
    network.http.sendRefererHeader = 0

## Disable Telemetry

    toolkit.telemetry.enabled = false
    toolkit.telemetry.unified = false
    toolkit.telemetry.archive.enabled = false
    toolkit.telemetry.shutdownPingSender.enabled = false
    toolkit.telemetry.firstShutdownPing.enabled = false
    toolkit.telemetry.updatePing.enabled = false
    toolkit.telemetry.newProfilePing.enabled = false
    toolkit.telemetry.bhrPing.enabled = false
    browser.ping-centre.telemetry = false
    browser.newtabpage.activity-stream.feeds.telemetry = false
    browser.newtabpage.activity-stream.telemetry = false

## Disable Pocket

    extensions.pocket.enabled = false
    services.sync.prefs.sync.browser.newtabpage.activity-stream.section.highlights.includePocket = false

## Enable Containers

    privacy.userContext.enabled = true
    privacy.userContext.ui.enabled = true

## Disable Disk Persistence

    browser.cache.disk.enable = false
    browser.privatebrowsing.forceMediaMemoryCache = true

## Others

    pdfjs.enableScripting = false    // Disable Javascript on PDF files
    geo.enabled = false              // Disable Geolocation
    dom.battery.enabled = false      // Disable Battery Status API

    network.dns.disablePrefetch = true
    network.prefetch-next = false
    
    gfx.webrender.all = true // New GPU renderer written in Rust

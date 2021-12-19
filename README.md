# 🦊 Firefox Advanced Settings

🦊 Firefox advanced settings for increased privacy 👁️  and security 🔒.

🚧 Work in progress...

## Configure DNS over HTTPS

    // Use DoH without fallback to insecure DNS
    network.trr.mode = 3

    // Use your prefered DoH server
    network.trr.uri = https://dns.paesa.es/dns-query
    network.trr.useGET = true

## Enable HTTPS-Only Mode

    dom.security.https_only_mode = true
    dom.security.https_only_mode_ever_enabled = true

## Enable HTTP3 (HTTP-over-QUIC) Protocol

    network.http.http3.enabled = true

## SSL/TLS Hardening

    // Disable TLS 1.0 and TLS 1.1
    security.tls.version.min = 3
    
    // Enable TLS Delegated Credentials
    security.tls.enable_delegated_credentials = true

    // Disable weak ciphersuites
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

    // Enable Encrypted Client Hello (ECH/ESNI)
    network.dns.echconfig.enabled = true
    network.dns.http3_echconfig.enabled = true
    network.dns.use_https_rr_as_altsvc = true

    // Disable OCSP checks
    security.OCSP.enabled = 0
    security.OCSP.require = false

    // Enforce CRLite revocation checks
    security.pki.crlite_mode = 2

## Sandbox

    // Enable Site Isolation
    fission.autostart = true

    // Windows only process hardening - Experimental
    security.sandbox.content.win32k-disable = true
    security.sandbox.gmp.win32k-disable = true
    security.sandbox.content.shadow-stack.enabled = true
    security.sandbox.gmp.shadow-stack.enabled = true
    security.sandbox.gpu.shadow-stack.enabled = true
    security.sandbox.gpu.level = 1

## Privacy Tweaks

    // Reject all Third-Party cookies
    network.cookie.cookieBehavior = 1

    // Disable Referer header
    network.http.sendRefererHeader = 0

    // Send DoNotTrack
    privacy.donottrackheader.enabled = true

    // Configure Tracking Protection
    privacy.trackingprotection.enabled = true
    privacy.trackingprotection.fingerprinting.enabled = true
    privacy.trackingprotection.cryptomining.enabled = true
    privacy.trackingprotection.socialtracking.enabled = true
    privacy.socialtracking.block_cookies.enabled = true

    // Enable First-Party Isolation
    privacy.firstparty.isolate = true

    // Resist browser fingerprinting
    privacy.resistFingerprinting = true
    privacy.spoof_english = 2

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

    gfx.webrender.all = true    // New GPU renderer written in Rust

    pdfjs.enableScripting = false    // Disable Javascript on PDF files
    geo.enabled = false              // Disable Geolocation
    dom.battery.enabled = false      // Disable Battery Status API

    network.dns.disablePrefetch = true
    network.prefetch-next = false

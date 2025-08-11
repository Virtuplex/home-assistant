# Production Dockerfile for Home Assistant addon
# Uses pre-built image from registry - no building on target device

ARG BUILD_FROM
FROM ${BUILD_FROM}

# Copy Home Assistant specific rootfs (needed for S6 overlay)
COPY rootfs /

# Labels for Home Assistant
ARG VERSION=dev
LABEL \
    io.hass.name="NanoKVM Dashboard" \
    io.hass.description="Dashboard for NanoKVM servers with previews and easy switching" \
    io.hass.arch="aarch64" \
    io.hass.type="addon" \
    io.hass.version="${VERSION}"

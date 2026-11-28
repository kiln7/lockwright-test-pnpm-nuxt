FROM node:lts@sha256:f8e5d4bb28fa55c74f1345166a082a10b7c68f22304350c1ce0d18358ae94996

RUN apt-get update && \
    apt-get install -fy libnss3 libnspr4 libatk1.0-0 libatk-bridge2.0-0 libcups2 libdbus-1-3 libdrm2 libxkbcommon0 libatspi2.0-0 libxcomposite1 libxdamage1 libxfixes3 libxrandr2 libgbm1 libasound2 && \
    apt-get clean autoclean && \
    apt-get autoremove --yes && \
    rm -rf /var/lib/{apt,dpkg,cache,log}

RUN corepack enable && npx playwright install

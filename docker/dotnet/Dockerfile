FROM microsoft/dotnet:2.2-sdk

WORKDIR /app

RUN echo check_certificate = off > /root/.wgetrc

# https://github.com/OmniSharp/omnisharp-vscode/wiki/Attaching-to-remote-processes
RUN apt-get update && apt-get install -y --no-install-recommends \
    unzip

# https://tech.tanaka733.net/entry/2017/05/04/clrdbg_has_been_replaced_with_vsdbg
RUN curl -sSLk https://aka.ms/getvsdbgsh | bash /dev/stdin -v latest -l ~/vsdbg
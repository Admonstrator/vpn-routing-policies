# VPN Routing policies for GL.iNET routers

This repository contains routing policies for GL.iNET routers. The policies are used to exclude certain domains from the VPN tunnel. This is useful if you need access streaming services that are blocked when using a VPN. Main usage in Germany.

This list is not complete and will be updated from time to time. Feel free to contribute.

## How to use

1. Copy and paste the desired policy into the "Custom Domain" field of the VPN policy.
2. Save and apply the policy.

## Policies

_The one marked as personal are used by me and may not be useful for you._

```plain
#START PERSONAL#
1password.com
1password.eu
mailbox.org
#END PERSONAL#
#START DISNEYPLUS#
disneyplus.com
bamgrid.com
bam.nr-data.net
cdn.registerdisney.go.com
cws.conviva.com
d9.flashtalking.com
disney-portal.my.onetrust.com
disneyplus.bn5x.net
disney-plus.net
dssott.com
adobedtm.com
#END DISNEYPLUS#
#START RTL+#
vodnowusoawsdash-cf.tvnow.de
playerconfig.player.tvnow.de
streamcheck.tvnow.de
player.tvnow.de
tvnow.de
rtl.de
vtrtl.de
widevine.tvnow.de
aws-cbc.cloud
#END RTL+#
```
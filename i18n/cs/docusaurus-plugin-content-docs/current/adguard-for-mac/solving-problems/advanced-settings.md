---
title: Průvodce pokročilými nastaveními
sidebar_position: 9
---

## Jak dosáhnout pokročilých nastavení

> Změna *Nízkoúrovňových nastavení* může způsobit problémy s výkonem AdGuardu, může přerušit internetové připojení nebo ohrozit vaši bezpečnost a soukromí. Tuto část byste měli otevřít pouze v případě, že jste si jisti tím, co děláte, nebo pokud se vás na to zeptal náš tým podpory. Chcete-li přejít na *Pokročilá nastavení*, postupujte takto: ikona AdGuardu v menu → ikona ozubeného kola → Pokročilé → Pokročilá nastavení.

## Pokročilá nastavení

`network.extension.exclude.domains`

The listed domains will be excluded from filtering in the *Network Extension* mode. Pro oddělení hodnot použijte čárku nebo zalomení řádku.

`network.extension.exclude.ports`

The listed ports will be excluded from filtering in the *Network Extension* mode. Pro oddělení hodnot použijte čárku nebo zalomení řádku.

`network.extension.route.exclude`

The listed routes will be excluded from filtering in the *Network Extension* mode. Nastavte routery pomocí IP adresy nebo cílového CIDR. Hodnoty oddělujte čárkami nebo zalomením řádků.

`network.extension.http.downgrade.bundleids`

Zde můžete zadat seznam aplikací, pro které bude protokol HTTP/2 v režimu filtrování *Rozšíření sítě* ponížen na HTTP/1.1. ID svazku by mělo být odděleno čárkou nebo zalomením řádku.

`network.extension.monterey.force.split.tunnel`

Here you can prohibit AdGuard from using the "default route" which is enabled by default in the *Network Extension* mode on macOS Monterey. AdGuard uses "default route" to disable iCloud Private Relay and Protect Mail Activity, as it cannot operate in unison with them.

Více informací o tomto problému najdete v [tomto článku](../icloud-private-relay).

`network.extension.dns.redirect.exclude.bundleids`

Zde můžete zadat seznam aplikací, které provádějí dotazy DNS přímo, nikoli prostřednictvím systémového DNS řešitele (například někteří klienti VPN nebo aplikace pro filtrování DNS). DNS filtrování pro ně bude zakázáno v režimu *Rozšíření sítě*. ID svazku by mělo být odděleno čárkou nebo zalomením řádku.

`network.dns.filter.secure.request`

Přesměruje zabezpečené DNS požadavky na místní DNS proxy, pokud je k dispozici.

`network.https.ocsp.check`

Nastavením `true` povolíte kontrolu odvolání certifikátu HTTPS.

`network.tcp.keepalive.enabled`

Pravidelně odesílá pakety TCP přes neaktivní připojení, aby se zajistilo aktivity a obnovení časových limitů NAT.

`network.tcp.keepalive.interval.seconds`

Doba nečinnosti v sekundách před odesláním udržovací sondy. Pokud je zadána 0, systém použije výchozí hodnotu.

`network.tcp.keepalive.timeout.seconds`

Doba v sekundách před odesláním další udržovací sondy neodpovídajícímu partnerovi. Pokud je zadána 0, použije se hodnota vybraná systémem.

`network.https.ech.enabled`

Používá místní DNS proxy k vyhledání konfigurací v seznamech konfigurací ECH. Pokud je nalezeno, zašifruje ClientHellos.

`network.https.enforce.certificate.transparency`

Ověřuje pravost všech certifikátů pro doménu na základě zásad transparentnosti certifikátů Chrome.

`network.filtering.localnetwork`

Nastavením `true` povolíte filtrování lokální sítě.

`network.filtering.localhost`

Nastavením `true` povolíte filtrování LoopBack.

`dns.proxy.bootstrap.ips`

Zde můžete zadat IP adresy DNS serverů, které budou použity k určení adresy šifrovaného DNS serveru.

`dns.proxy.fallback.ips`

Zde můžete zadat seznam IP adres DNS serverů, které budou použity jako zálohy v případě, že šifrovaný DNS server neodpoví.

`dns.proxy.fallback.on.upstreams.failure.enabled`

Běžné dotazy budou přesměrovány do odchozího připojení, pokud všechny běžné dotazy v odchozím připojení selžou.

`dns.proxy.detect.search.domains`

Tato možnost umožňuje automatickou detekci domény lokální sítě, která bude automaticky přesměrována na záložní DNS server namísto hlavního DNS serveru.

`dns.proxy.fallback.domains`

Zde můžete uvést seznam domén, pro které bude použit záložní DNS server namísto hlavního DNS serveru.

`dns.proxy.adblockrules.blocking.mode`

Zde můžete zadat typ odezvy DNS serveru na blokované požadavky odpovídající pravidlům typu ad-blocker.

* 0 — odezva s REFUSED
* 1 — odezva s NXDOMAIN
* 2 — odezva s 0.0.0.0 nebo adresou uvedenou v `dns.proxy.blocking.response.IPv4.address` a/nebo `dns.proxy.blocking.response.IPv6.address`

`dns.proxy.hostrules.blocking.mode`

Zde můžete zadat typ odezvy DNS serveru na blokované požadavky odpovídající pravidlům typu hosts:

* 0 — odezva s REFUSED
* 1 — odezva s NXDOMAIN
* 2 — odezva s 0.0.0.0 nebo adresou uvedenou v `dns.proxy.blocking.response.IPv4.address` a/nebo `dns.proxy.blocking.response.IPv6.address`

`dns.proxy.blocking.response.IPv4.address`

Zde můžete zadat adresu IPv4, která bude vrácena jako odezva na blokované požadavky "A", pokud je `dns.proxy.adblockrules.blocking.mode` nebo `dns.proxy.hostrules.blocking.mode` nastaven na typ odezvy "ADDRESS".

`dns.proxy.blocking.response.IPv6.address`

Zde můžete zadat adresu IPv6, která bude vrácena jako odezva na blokované požadavky "AAAA", pokud je `dns.proxy.adblockrules.blocking.mode` nebo `dns.proxy.hostrules.blocking.mode` nastaven na typ odezvy "ADDRESS".

`dns.proxy.block.AAAA.requests`

Zde můžete povolit blokování DNS dotazů IPv6.

`dns.proxy.blocked.response.TTL.in.seconds`

Zde můžete zadat hodnotu TTL (time to live), která bude vrácena jako odpověď na zablokovaný požadavek.

`dns.proxy.parallel.upstream.queries.enabled`

Všechna odchozí připojení jsou dotazována současně. První odezva je vrácena.

`dns.proxy.servfail.on.upstreams.failure.enabled`

Reaguje na selhání odchozího připojení paketem SERVFAIL.

`dns.proxy.http3.enabled`

Povolí HTTP/3 pro odchozí připojení DNS-over-HTTPS pro zrychlení připojení.

`dns.proxy.block.encrypted.client.hello.response`

Odstraní z dotazů parametry Encrypted Client Hello.

`stealth.antidpi.http.split.fragment.size`

Upraví velikost fragmentace požadavků HTTP. Povolené hodnoty: 1–1500. Pokud je zadána neplatná velikost, systém použije výchozí hodnotu.

`stealth.antidpi.clienthello.split.fragment.size`

Tato možnost určuje velikost fragmentace TCP paketů, což pomáhá vyhnout se hluboké kontrole paketů. Povolené hodnoty: 1–1500. Pokud je zadána neplatná velikost, systém použije výchozí hodnotu.

`stealth.antidpi.http.space.juggling`

Přidá dodatečnou mezeru mezi metodu HTTP a URL adresu a odstraní mezeru za polem "Host:"

`subscription.link.interception.userscript`

Tuto funkci aktivujte, pokud chcete, aby AdGuard automaticky zachycoval adresy URL uživatelských skriptů a otevíral instalační okno.

`subscription.link.interception.filter`

Tuto funkci aktivujte, pokud chcete, aby AdGuard automaticky zachycoval adresy URL odběru (například abp:subscribe atd.) a otevřel okno nastavení vlastního filtru.

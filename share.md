zone "c.secrank.cn" {
    type master;
    file "/etc/bind/zones/db.c.secrank.cn";
};

;
; BIND data file for local loopback interface
$TTL    10
@       IN      SOA     ns.c.secrank.cn. root.c.secrank.cn. (
2      ; Serial
604800    ; Refresh
86400    ; Retry
2419200    ; Expire
604000)   ; Negative Cache TTL
;
;
; name servers - NS records
@    IN      NS      ns.c.secrank.cn.
@    IN      A       10.0.1.32
ns   IN      A       10.0.1.32
www          IN      A      10.0.1.32

aiemu        IN      A      10.0.1.32
hgd17        IN      A      10.0.1.32

sudo certbot certonly --standalone -d web.zz17.c.secrank.cn -d web.hegd17.c.secrank.cn --server https://ca.course.secrank.cn/acme/acme/directory


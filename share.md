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

; BIND data file for local loopback interface
$TTL    60
@       IN      SOA     zz17.c.secrank.cn. root.zz17.c.secrank.cn. (
2      ; Serial
604800    ; Refresh
86400    ; Retry
2419200    ; Expire
60)   ; Negative Cache TTL
;
;
; name servers - NS records
@    IN      NS      ns.zz17.c.secrank.cn.
zz17.c.secrank.cn.    IN      A       10.0.1.32
ns.zz17.c.secrank.cn.   IN      A       10.0.1.32
web.zz17.c.secrank.cn.  IN      A       10.0.1.32


; BIND data file for local loopback interface
$TTL    60
@       IN      SOA     hegd17.c.secrank.cn. root.hegd17.c.secrank.cn. (
2      ; Serial
604800    ; Refresh
86400    ; Retry
2419200    ; Expire
60)   ; Negative Cache TTL
;
;
; name servers - NS records
@    IN      NS      ns.hegd17.c.secrank.cn.
hegd17.c.secrank.cn.    IN      A       10.0.1.32
ns.hegd17.c.secrank.cn.   IN      A       10.0.1.32
web.hegd17.c.secrank.cn.  IN      A       10.0.1.32



zone "zz17.c.secrank.cn" {
    type master;
    file "/etc/bind/zones/db.zz17.c.secrank.cn";
};

zone "hegd17.c.secrank.cn" {
    type master;
    file "/etc/bind/zones/db.hegd17.c.secrank.cn";
};




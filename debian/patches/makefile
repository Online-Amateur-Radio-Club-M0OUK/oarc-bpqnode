--- a/makefile
+++ b/makefile
@@ -29,11 +29,15 @@
 	
 linbpq: $(OBJS)
 	gcc $(OBJS) -Xlinker -Map=output.map -l:libminiupnpc.a -lrt -lm -lz -lpthread -lconfig -lpcap -o linbpq
-	sudo setcap "CAP_NET_ADMIN=ep CAP_NET_RAW=ep CAP_NET_BIND_SERVICE=ep" linbpq		
+#	setcap "CAP_NET_ADMIN=ep CAP_NET_RAW=ep CAP_NET_BIND_SERVICE=ep" linbpq		
+
+install: 
+	install -b -m 755  -D -d		debian/linbpq/usr/sbin
+	install -b -m 755  -s -p linbpq		debian/linbpq/usr/sbin
 
 -include *.d
 
 clean :
-	rm *.d
-	rm linbpq $(OBJS)
+	rm -f *.d
+	rm -f linbpq $(OBJS)
 

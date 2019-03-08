V := 01
ID := draft-friel-tls-atls-$(V)

$(ID).txt: $(ID).xml
	xml2rfc -q $< -o $@

$(ID).xml: $(ID).md
	cat $< | kramdown-rfc2629 > $@

clean:
	$(RM) $(ID).xml $(ID).txt

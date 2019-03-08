V := 01
ID := draft-friel-tls-atls-$(V)

all: $(ID).txt

$(ID).xml: $(ID).md ; cat $< | kramdown-rfc2629 > $@

$(ID).txt: $(ID).xml ; xml2rfc -q $< -o $@

clean: ; $(RM) $(ID).xml $(ID).txt

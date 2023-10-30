# go-xcm
Go bindings for Ericsson xcm library


## Add this to tar for installing XCM in an xcluster ovl
```
test -n "$XCM_DIR" || XCM_DIR=$GOPATH/src/github.com/Ericsson/xcm
log "Installing XCM from $XCM_DIR"
(cd $XCM_DIR; ./configure --prefix=/ --disable-lttng > /dev/null 2>&1 || die "Failed to configure xcm")
make -C $XCM_DIR > /dev/null 2>&1 || die "Failed to make xcm"
DESTDIR=$tmp make -C $XCM_DIR install > /dev/null 2>&1 || die "Failed to install xcm"
```

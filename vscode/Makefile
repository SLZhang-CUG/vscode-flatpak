all:
	# Install dependencies
	./scripts/npm.sh install
	./scripts/npm.sh add gm
	# build vscode
	./node_modules/.bin/gulp vscode-linux-${VSCODE_ARCH}-prepare-flatpak --max_old_space_size=4096

install:
	cp -ar .build/linux/flatpak/${FLATPAK_ARCH}/* /app/
	ln -sf /app/share/code/bin/code-oss /app/bin/code-oss

.PHONY: all install

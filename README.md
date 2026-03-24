# 设置默认输入法框架为 fcitx5
im-config -n fcitx5

# 添加开机自启（防止登录后无图标）
mkdir -p ~/.config/autostart
cat > ~/.config/autostart/fcitx5.desktop <<EOF
[Desktop Entry]
Type=Application
Exec=fcitx5 -d
Hidden=false
NoDisplay=false
X-GNOME-Autostart-enabled=true
Name=Fcitx5
Comment=Start Fcitx5 input method
EOF

# 重启系统
reboot

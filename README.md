# Hyprland_Space_Retro
Hyprland Space Retro

![Screen 1](img/11.png)
![Screen 2](img/12.png)
![Screen 1](img/21.png)
![Screen 2](img/22.png)
![Screen 1](img/31.png)
![Screen 2](img/32.png)


###################
### KEYBINDINGS ###
###################

$mainMod = SUPER

# Приложения и система
bind = $mainMod, Return, exec, $terminal
bind = $mainMod, Q, killactive,
bind = $mainMod, N, exec, firefox
bind = $mainMod, T, exec, Telegram
bind = $mainMod, E, exec, thunar
bind = $mainMod, D, exec, wofi --show drun
bind = CTRL ALT, Delete, exit,
bind = $mainMod SHIFT, F, fullscreen,
bind = $mainMod ALT, F, togglefloating,
bind = $mainMod, G, togglegroup,

bind = $mainMod CTRL SHIFT, R, exec, killall waybar
bind = $mainMod SHIFT, R, exec, waybar

# Утилиты
bind = CTRL ALT, L, exec, swaylock                # Блокировка

# Скриншоты (нужны grim, slurp, swappy)
bind = , Print, exec, grim - | swappy -f -
# # То же самое на Win+Shift+S (как в Windows)
bind = $mainMod SHIFT, S, exec, grim -g "$(slurp)" - | swappy -f -

# Обои (Swww)
bind = CTRL ALT, W, exec, ~/.config/hypr/scripts/wall.sh


# Навигация (Фокус)
bind = $mainMod, left, movefocus, l
bind = $mainMod, right, movefocus, r
bind = $mainMod, up, movefocus, u
bind = $mainMod, down, movefocus, d
bind = ALT, Tab, movefocus, d

# Перемещение окон (Move)
bind = $mainMod CTRL, left, movewindow, l
bind = $mainMod CTRL, right, movewindow, r
bind = $mainMod CTRL, up, movewindow, u
bind = $mainMod CTRL, down, movewindow, d

# Ресайз (Resize)
bind = $mainMod SHIFT, left, resizeactive, -40 0
bind = $mainMod SHIFT, right, resizeactive, 40 0
bind = $mainMod SHIFT, up, resizeactive, 0 -40
bind = $mainMod SHIFT, down, resizeactive, 0 40

# Воркспейсы
bind = $mainMod, 1, workspace, 1
bind = $mainMod, 2, workspace, 2
bind = $mainMod, 3, workspace, 3
bind = $mainMod, 4, workspace, 4
bind = $mainMod, 5, workspace, 5
bind = $mainMod, 6, workspace, 6
bind = $mainMod, 7, workspace, 7
bind = $mainMod, 8, workspace, 8
bind = $mainMod, 9, workspace, 9
bind = $mainMod, 0, workspace, 10
bind = $mainMod, Tab, workspace, e+1
bind = $mainMod SHIFT, Tab, workspace, e-1

# Перемещение в воркспейс + переход
bind = $mainMod SHIFT, 1, movetoworkspace, 1
bind = $mainMod SHIFT, 2, movetoworkspace, 2
bind = $mainMod SHIFT, 3, movetoworkspace, 3
bind = $mainMod SHIFT, 4, movetoworkspace, 4
bind = $mainMod SHIFT, 5, movetoworkspace, 5
bind = $mainMod SHIFT, 6, movetoworkspace, 6
bind = $mainMod SHIFT, 7, movetoworkspace, 7
bind = $mainMod SHIFT, 8, movetoworkspace, 8
bind = $mainMod SHIFT, 9, movetoworkspace, 9
bind = $mainMod SHIFT, 0, movetoworkspace, 10

# Специальный воркспейс (Scratchpad)
bind = $mainMod, U, togglespecialworkspace,
bind = $mainMod SHIFT, U, movetoworkspace, special

# Мышь
bindm = $mainMod, mouse:272, movewindow
bindm = $mainMod, mouse:273, resizewindow

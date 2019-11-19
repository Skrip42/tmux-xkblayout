# tmux-xkblayout
show current locale, CapsLock and NumLock in your status bar.

### Installation
- install xkeyboard-check: https://github.com/Skrip42/xkeyboard-check
- clone the repo: git clone https://github.com/Skrip42/tmux-xkblayout.git ~/clone/path
- add this line in your .tmux.conf: run-shell ~/clone/path/xkblayout.tmux
- reload tmux environment

### Usage
- #{xkeyboard_locale} - print current locale
- #{xkeyboard_isCapsLock} - if `CapsLock` enabled print 1 else 0
- #{xkeyboard_isNumLock} - if `NumLock` enabled print 1 else 0

your can use it like: 
`set-option -g status-right '#{?#{xkeyboard_isNumLock},#[bg=green] NL #[bg=black],}#{?#{xkeyboard_isCapsLock},#[bg=red] CL  #[bg=black],} #{xkeyboard_locale}` in your .tmux.conf

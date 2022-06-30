% killall Dock
% defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'; killall Dock
% defaults write com.apple.dock static-only -bool true; killall Dock
% defaults write com.apple.dock single-app -bool true; killall Dock
% defaults write com.apple.Dock showhidden -bool yes; killall Dock
% defaults write com.apple.dock mineffect -string suck; killall Dock
% defaults write com.apple.dock largesize -int 512; killall Dock
% defaults write com.apple.dock tilesize -integer 8; killall Dock
% defaults write com.apple.dock autohide-time-modifier -float 1; killall Dock
% defaults write com.apple.dock autohide-delay -float 0; killall Dock
% defaults write com.apple.dock autohide-time-modifier -float 0.4; killall Dock
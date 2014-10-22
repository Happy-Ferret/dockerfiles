FROM ubuntu:14.04

RUN apt-get -y update
RUN apt-get -y install zsh
RUN apt-get -y install git
RUN apt-get -y install ruby
RUN apt-get -y install python
RUN apt-get -y install vim
RUN apt-get -y install tmux
RUN apt-get -y install curl
RUN apt-get -y install wget

RUN useradd marcelo
RUN mkdir /home/marcelo && chown -R marcelo: /home/marcelo

WORKDIR /home/marcelo
ENV HOME /home/marcelo

RUN git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
RUN git clone https://github.com/altercation/vim-colors-solarized.git ~/.vim/bundle/vim-colors-solarized
RUN git clone https://github.com/marceloandrader/dotfiles.git .dotfiles
RUN chown -R marcelo: .dotfiles
RUN chown -R marcelo: .vim
RUN ln -s ~/.dotfiles/tmux/tmux.conf.symlink .tmux.conf
RUN ln -s ~/.dotfiles/zsh/zshrc.symlink .zshrc
RUN ln -s ~/.dotfiles/vim/vimrc.symlink .vimrc
RUN vim +PluginInstall +qall

USER marcelo
CMD ["zsh"]

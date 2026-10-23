cask_args appdir: "/Applications", require_sha: true

# Mac App Store command line interface
brew "mas" # Mac App Store command-line interface | https://github.com/mas-cli/mas

# Loads every category file (*.Brewfile). Use `bbrew -f <file>` to manage one interactively.
Dir[File.join(__dir__, '*.Brewfile')].sort.each do |file|
  instance_eval(File.read(file), file)
end

ENEMIES = [
  "python sample_bots/GreedyBot.py",
  "python sample_bots/HoldBot.py",
  "python sample_bots/RandomBot.py"
]

task :play do
  turns = ENV["TURNS"] || "1000"

  Dir.chdir('runner') do
    command = [
      "./playgame.py",
      "--player_seed 42",
      "--end_wait=0.25",
      "--log_dir ../log",
      "--turns #{turns}",
      "--log_stderr",
      "--verbose",
      "--map_file ../maps/symmetric_maps/symmetric_10.map",
      '"ruby ../MyBot.rb"',   
      '"python ../sample_bots/GreedyBot.py"',
      '"python ../sample_bots/GreedyBot.py"',
      '"python ../sample_bots/LeftyBot.py"'
    ]
    sh command.join(' ')
  end
end

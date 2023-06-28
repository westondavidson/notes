
        private void Seed()
        {
            using (var context = new MixerDBContext(options))
            {
                context.Database.EnsureDeleted();
                context.Database.EnsureCreated();


                context.User.AddRange
                    (
                    new User
                    {
                        Id = 1,
                        UserName = "WestonD123",
                        Email = "westondavidson@outlook.com",
                        IsAdmin = true

                    },
                    new User
                    {
                        Id = 2,
                        UserName = "JackLongDog",
                        Email = "jacklong@gmail.com",
                        IsAdmin = false

                    }
                    );


                context.SavedProject.AddRange(
                    new SavedProject
                    {
                        Id = 1,
                        ProjectName = "epic project",
                        BPM = 140
                    },
                    new SavedProject
                    {
                        Id = 2,
                        ProjectName = "insane_3242020_V3",
                        BPM = 160
                    }
                    );

                context.UserProject.AddRange(
                    new UserProject
                    {
                        Id = 1,
                        UserId = 1,
                        ProjectId = 1,
                        Owner = true
                    },
                    new UserProject
                    {
                        Id = 2,
                        UserId = 2,
                        ProjectId = 1,
                        Owner = false
                    }

                    );

                context.Sample.AddRange(
                    new Sample
                    {
                        Id = 1,
                        UserId = 1,
                        SampleName = "snare_4",
                        SampleLink = "snare_4"

                    },
                    new Sample
                    {
                        Id = 2,
                        UserId = 2,
                        SampleName = "kick_8",
                        SampleLink = "kick_8"

                    }
                    );

                context.Pattern.AddRange(
                    new Pattern
                    {
                        Id = 2,
                        PatternData = "10110111"
                    },
                    new Pattern
                    {
                        Id = 3,
                        PatternData = "00010001"
                    }


                    );
                context.Track.AddRange(
                    new Track
                    {
                        Id = 1,
                        ProjectId = 1,
                        SampleId = 1,
                        PatternId = 2
                    },
                    new Track
                    {
                        Id = 2,
                        ProjectId = 1,
                        SampleId = 2,
                        PatternId = 3
                    },
                    new Track
                    {
                        Id = 3,
                        ProjectId = 2,
                        SampleId = 1,
                        PatternId = 2
                    }

                    );

                context.PlayList.AddRange(
                    new PlayList
                    {
                        Id = 1,
                        UserId = 1,
                        Name = "Sick EDM"
                    },
                    new PlayList
                    {
                        Id = 2,
                        UserId = 2,
                        Name = "Country"
                    }

                    );

                context.UploadMusic.AddRange(
                    new UploadMusic
                    {
                        Id = 1,
                        UserId = 1,
                        MusicFilePath = "cool_song",
                        Name = "Jumping Jacks",
                        UploadDate = DateTime.Parse("2021-03-15 18:17:00"),
                        Likes = 3409,
                        Plays = 90845


                    },
                    new UploadMusic
                    {
                        Id = 2,
                        UserId = 2,
                        MusicFilePath = "crazy_mix",
                        Name = "BBCRadio1Xtra Mix - Jack",
                        UploadDate = DateTime.Parse("2021-03-16 18:18:00"),
                        Likes = 8709,
                        Plays = 3937829
                    }

                    );

                context.Comments.AddRange(
                    new Comments
                    {
                        Id = 1,
                        Comment = "wow this song is so sick what the heck!",
                        CommentData = DateTime.Parse("2021-03-15 18:17:00"),
                        UserId = 2,
                        UploadMusicId = 1
                    },
                    new Comments
                    {
                        Id = 2,
                        Comment = "what.. this song transition... amazing!",
                        CommentData = DateTime.Parse("2021-03-15 18:17:00"),
                        UserId = 1,
                        UploadMusicId = 2
                    }

                    );
                context.MusicPlaylist.AddRange(
                    new MusicPlaylist
                    {
                        Id = 1,
                        PlayListId = 1,
                        MusicId = 1,
                    },
                    new MusicPlaylist
                    {
                        Id = 2,
                        PlayListId = 1,
                        MusicId = 2
                    },
                    new MusicPlaylist
                    {
                        Id = 3,
                        PlayListId = 2,
                        MusicId = 1
                    }

                    );
            }
        }
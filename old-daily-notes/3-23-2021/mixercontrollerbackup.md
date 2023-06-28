using Microsoft.AspNetCore.Mvc;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using MixerBL;
using MixerModels;

namespace MixerREST.Controllers
{
    /// <summary>
    /// This is the REST API for our RevMixer application
    /// </summary>
    [Route("api/[controller]")]
    [ApiController]
    public class MixerController : ControllerBase
    {
        private readonly IMixerBL _mixerBL;
        //UploadedMusic
        //Users
        //SavedProjects
        //Sample
        //Tracks
        //Paterns
        public MixerController(IMixerBL mixerBL)
        {
            _mixerBL = mixerBL;
        }
        // GET: api/Mixer/AllUploadedMusic
        [HttpGet]
        [Route("AllUploadedMusic")]
        public async Task<IActionResult> GetUploadedMusicAsync()
        {
            return Ok(await _mixerBL.GetUploadedMusicAsync());
        }
        //GET: api/Mixer/GetAllUsers
        [HttpGet]
        [Route("GetAllUsers")]
        public async Task<IActionResult> GetUsersAsync()
        {
            return Ok(await _mixerBL.GetUsersAsync());
        }
        //GET: api/Mixer/GetAllSavedProjects
        [HttpGet]
        [Route("GetAllSavedProjects")]
        public async Task<IActionResult> GetSavedProjectsAsync()
        {
            return Ok(await _mixerBL.GetSavedProjectsAsync());
        }
        //GET: api/Mixer/GetAllSamples
        [HttpGet]
        [Route("GetAllSamples")]
        public async Task<IActionResult> GetSamplesAsync()
        {
            return Ok(await _mixerBL.GetSamplesAsync());
        }
        //GET: api/Mixer/GetAllTracks
        [HttpGet]
        [Route("GetAllTracks")]
        public async Task<IActionResult> GetTracksAsync()
        {
            return Ok(await _mixerBL.GetTracksAsync());
        }
        //GET: api/Mixer/GetAllPatterns
        [HttpGet]
        [Route("GetAllPatterns")]
        public async Task<IActionResult> GetPatternsAsync()
        {
            return Ok(await _mixerBL.GetPatternsAsync());
        }
        //GET: api/Mixer/GetAllUserProjects
        [HttpGet]
        [Route("GetAllUserProjects")]
        public async Task<IActionResult> GetUserProjectsAsync()
        {
            return Ok(await _mixerBL.GetUserProjectsAsync());
        }
        //GET: api/Mixer/GetAllPlayLists
        [HttpGet]
        [Route("GetAllPlayLists")]
        public async Task<IActionResult> GetPlayListsAsync()
        {
            return Ok(await _mixerBL.GetPlayListsAsync());
        }
        //GET: api/Mixer/GetAllMusicPlayLists
        [HttpGet]
        [Route("GetAllMusicPlayLists")]
        public async Task<IActionResult> GetMusicPlaylistsAsync()
        {
            return Ok(await _mixerBL.GetMusicPlaylistsAsync());
        }
        //GET: api/Mixer/GetAllComments
        [HttpGet]
        [Route("GetAllComments")]
        public async Task<IActionResult> GetCommentsAsync()
        {
            return Ok(await _mixerBL.GetCommentsAsync());
        }
        // GET api/Mixer/GetUploadedMusicByID/1
        [HttpGet]
        [Route("GetUploadedMusicByID/{uploadedMusicID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetUploadedMusicByIDAsync(int uploadedMusicID)
        {
            var uploadedMusic = await _mixerBL.GetUploadedMusicByIDAsync(uploadedMusicID);
            if (uploadedMusic == null) return NotFound();
            return Ok(uploadedMusic);
        }
        // GET api/Mixer/GetUserByID/1
        [HttpGet]
        [Route("GetUserByID/{userID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetUserByIDAsync(int userID)
        {
            var user = await _mixerBL.GetUserByIDAsync(userID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // GET api/Mixer/GetSavedProjectByID/1
        [HttpGet]
        [Route("GetSavedProjectByID/{savedProjectID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetSavedProjectByIDAsync(int savedProjectID)
        {
            var user = await _mixerBL.GetSavedProjectByIDAsync(savedProjectID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // GET api/Mixer/GetSampleByID/1
        [HttpGet]
        [Route("GetSampleByID/{sampleID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetSampleByIDAsync(int sampleID)
        {
            var user = await _mixerBL.GetSampleByIDAsync(sampleID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // GET api/Mixer/GetTrackByID/1
        [HttpGet]
        [Route("GetTrackByID/{trackID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetTrackByIDAsync(int trackID)
        {
            var user = await _mixerBL.GetTrackByIDAsync(trackID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // GET api/Mixer/GetPatternByID/1
        [HttpGet]
        [Route("GetPatternByID/{patternID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetPatternByIDAsync(int patternID)
        {
            var user = await _mixerBL.GetPatternByIDAsync(patternID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // GET api/Mixer/GetUserProjectByID/1
        [HttpGet]
        [Route("GetUserProjectByID/{userProjectID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetUserProjectByIDAsync(int userProjectID)
        {
            var user = await _mixerBL.GetUserProjectByIDAsync(userProjectID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // GET api/Mixer/GetPlayListByID/1
        [HttpGet]
        [Route("GetPlayListByID/{playlistID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetPlaylistByIDAsync(int playlistID)
        {
            var user = await _mixerBL.GetPlayListByIDAsync(playlistID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // GET api/Mixer/GetMusicPlayListByID/1
        [HttpGet]
        [Route("GetMusicPlayListByID/{musicPlayListID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetMusicPlaylistByIDAsync(int musicPlayListID)
        {
            var user = await _mixerBL.GetMusicPlaylistByIDAsync(musicPlayListID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // GET api/Mixer/GetCommentByID/1
        [HttpGet]
        [Route("GetCommentByID/{commentID}")]
        [Produces("application/json")]
        public async Task<IActionResult> GetCommentByIDAsync(int commentID)
        {
            var user = await _mixerBL.GetCommentByIDAsync(commentID);
            if (user == null) return NotFound();
            return Ok(user);
        }
        // POST api/Mixer/AddUploadedMusic
        [HttpPost]
        [Route("AddUploadedMusic")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddUploadedMusicAsync([FromBody] UploadMusic uploadedMusic)
        {
            try
            {
                await _mixerBL.AddUploadedMusicAsync(uploadedMusic);
                return CreatedAtAction("AddUploadedMusic", uploadedMusic);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddUser
        [HttpPost]
        [Route("AddUser")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddUserAsync([FromBody] User user)
        {
            try
            {
                await _mixerBL.AddUserAsync(user);
                return CreatedAtAction("AddUser", user);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddSavedProject
        [HttpPost]
        [Route("AddSavedProject")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddSavedProjectAsync([FromBody] SavedProject savedProject)
        {
            try
            {
                await _mixerBL.AddSavedProjectAsync(savedProject);
                return CreatedAtAction("AddSavedProject", savedProject);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddSample
        [HttpPost]
        [Route("AddSample")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddSampleAsync([FromBody] Sample sample)
        {
            try
            {
                await _mixerBL.AddSampleAsync(sample);
                return CreatedAtAction("AddSample", sample);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddTrack
        [HttpPost]
        [Route("AddTrack")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddTrackAsync([FromBody] Track track)
        {
            try
            {
                await _mixerBL.AddTrackAsync(track);
                return CreatedAtAction("AddTrack", track);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddPattern
        [HttpPost]
        [Route("AddPattern")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddPatternAsync([FromBody] Pattern pattern)
        {
            try
            {
                await _mixerBL.AddPatternAsync(pattern);
                return CreatedAtAction("AddPattern", pattern);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddUserProject
        [HttpPost]
        [Route("AddUserProject")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddUserProjectAsync([FromBody] UserProject userProject)
        {
            try
            {
                await _mixerBL.AddUserProjectAsync(userProject);
                return CreatedAtAction("AddUserProject", userProject);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddPlayList
        [HttpPost]
        [Route("AddPlayList")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddPlaylistAsync([FromBody] PlayList playlist)
        {
            try
            {
                await _mixerBL.AddPlayListAsync(playlist);
                return CreatedAtAction("AddPlaylist", playlist);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddMusicPlayList
        [HttpPost]
        [Route("AddMusicPlayList")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddMusicPlaylistAsync([FromBody] MusicPlaylist musicPlaylist)
        {
            try
            {
                await _mixerBL.AddMusicPlaylistAsync(musicPlaylist);
                return CreatedAtAction("AddMusicPlaylist", musicPlaylist);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // POST api/Mixer/AddComment
        [HttpPost]
        [Route("AddComment")]
        [Consumes("application/json")]
        public async Task<IActionResult> AddCommentAsync([FromBody] Comments comment)
        {
            try
            {
                await _mixerBL.AddCommentAsync(comment);
                return CreatedAtAction("AddComment", comment);
            }
            catch
            {
                return StatusCode(400);
            }
        }
        // PUT api/Mixer/UpdateUploadedMusic/1
        [HttpPut]
        [Route("UpdateUploadedMusic/{id}")]
        public async Task<IActionResult> UpdateUploadedMusicAsync(int id, [FromBody] UploadMusic uploadedMusic)
        {
            try
            {
                await _mixerBL.UpdateUploadedMusicAsync(uploadedMusic);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdateUser/1
        [HttpPut]
        [Route("UpdateUser/{id}")]
        public async Task<IActionResult> UpdateUserAsync(int id, [FromBody] User user)
        {
            try
            {
                await _mixerBL.UpdateUserAsync(user);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdateSavedProject/1
        [HttpPut]
        [Route("UpdateSavedProject/{id}")]
        public async Task<IActionResult> UpdateSavedProjectAsynch(int id, [FromBody] SavedProject savedProject)
        {
            try
            {
                await _mixerBL.UpdateSavedProjectAsync(savedProject);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdateSample/1
        [HttpPut]
        [Route("UpdateSample/{id}")]
        public async Task<IActionResult> UpdateSampleAsynch(int id, [FromBody] Sample sample)
        {
            try
            {
                await _mixerBL.UpdateSampleAsync(sample);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdateTrack/1
        [HttpPut]
        [Route("UpdateTrack/{id}")]
        public async Task<IActionResult> UpdateTrackAsynch(int id, [FromBody] Track track)
        {
            try
            {
                await _mixerBL.UpdateTrackAsync(track);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdatePattern/1
        [HttpPut]
        [Route("UpdatePattern/{id}")]
        public async Task<IActionResult> UpdatePatternAsynch(int id, [FromBody] Pattern pattern)
        {
            try
            {
                await _mixerBL.UpdatePatternAsync(pattern);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdateUserProject/1
        [HttpPut]
        [Route("UpdateUserProject/{id}")]
        public async Task<IActionResult> UpdateUserProjectAsynch(int id, [FromBody] UserProject userProject)
        {
            try
            {
                await _mixerBL.UpdateUserProjectAsync(userProject);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdatePlayList/1
        [HttpPut]
        [Route("UpdatePlayList/{id}")]
        public async Task<IActionResult> UpdatePlayListAsynch(int id, [FromBody] PlayList playList)
        {
            try
            {
                await _mixerBL.UpdatePlayListAsync(playList);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdateMusicPlayList/1
        [HttpPut]
        [Route("UpdateMusicPlayList/{id}")]
        public async Task<IActionResult> UpdateMusicPlaylistAsynch(int id, [FromBody] MusicPlaylist musicPlaylist)
        {
            try
            {
                await _mixerBL.UpdateMusicPlaylistAsync(musicPlaylist);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // PUT api/Mixer/UpdateComment/1
        [HttpPut]
        [Route("UpdateComment/{id}")]
        public async Task<IActionResult> UpdateCommentAsynch(int id, [FromBody] Comments comment)
        {
            try
            {
                await _mixerBL.UpdateCommentAsync(comment);
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeleteUploadedMusic
        [HttpDelete]
        [Route("DeleteUploadedMusic/{uploadedMusicID}")]
        public async Task<IActionResult> DeleteUploadedMusicAsync(int uploadedMusicID)
        {
            try
            {
                await _mixerBL.DeleteUploadedMusicAsync(await _mixerBL.GetUploadedMusicByIDAsync(uploadedMusicID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeleteUser
        [HttpDelete]
        [Route("DeleteUser/{userID}")]
        public async Task<IActionResult> DeleteUserAsync(int userID)
        {
            try
            {
                await _mixerBL.DeleteUserAsync(await _mixerBL.GetUserByIDAsync(userID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeleteSavedProject
        [HttpDelete]
        [Route("DeleteSavedProject/{savedProjectID}")]
        public async Task<IActionResult> DeleteSavedProjectAsync(int savedProjectID)
        {
            try
            {
                await _mixerBL.DeleteSavedProjectAsync(await _mixerBL.GetSavedProjectByIDAsync(savedProjectID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeleteSample
        [HttpDelete]
        [Route("DeleteSample/{sampleID}")]
        public async Task<IActionResult> DeleteSampleAsync(int sampleID)
        {
            try
            {
                await _mixerBL.DeleteSampleAsync(await _mixerBL.GetSampleByIDAsync(sampleID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeleteTrack
        [HttpDelete]
        [Route("DeleteTrack/{trackID}")]
        public async Task<IActionResult> DeleteTrackAsync(int trackID)
        {
            try
            {
                await _mixerBL.DeleteTrackAsync(await _mixerBL.GetTrackByIDAsync(trackID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeletePattern
        [HttpDelete]
        [Route("DeletePattern/{patternID}")]
        public async Task<IActionResult> DeletePatternAsync(int patternID)
        {
            try
            {
                await _mixerBL.DeletePatternAsync(await _mixerBL.GetPatternByIDAsync(patternID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeleteUserProject
        [HttpDelete]
        [Route("DeleteUserProject/{userProjectID}")]
        public async Task<IActionResult> DeleteUserProjectAsync(int userProjectID)
        {
            try
            {
                await _mixerBL.DeleteUserProjectAsync(await _mixerBL.GetUserProjectByIDAsync(userProjectID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeletePlayList
        [HttpDelete]
        [Route("DeletePlayList/{playListID}")]
        public async Task<IActionResult> DeletePlayListAsync(int playListID)
        {
            try
            {
                await _mixerBL.DeletePlayListAsync(await _mixerBL.GetPlayListByIDAsync(playListID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }
        // DELETE api/Mixer/DeleteMusicPlayList
        [HttpDelete]
        [Route("DeleteMusicPlayList/{musicPlayListID}")]
        public async Task<IActionResult> DeleteMusicPlaylistAsync(int musicPlayListID)
        {
            try
            {
                await _mixerBL.DeleteMusicPlaylistAsync(await _mixerBL.GetMusicPlaylistByIDAsync(musicPlayListID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }

        // DELETE api/Mixer/DeleteComment
        [HttpDelete]
        [Route("DeleteComment/{commentID}")]
        public async Task<IActionResult> DeleteCommentAsync(int commentID)
        {
            try
            {
                await _mixerBL.DeleteCommentAsync(await _mixerBL.GetCommentByIDAsync(commentID));
                return NoContent();
            }
            catch
            {
                return StatusCode(500);
            }
        }

    }
}

# StoryReaction

**Description** : *How a certain peer reacted to or interacted with a story*

**Layer** : 211

```tl
storyReaction#6090d6d5 peer_id:Peer date:int reaction:Reaction = StoryReaction;
storyReactionPublicForward#bbab2643 message:Message = StoryReaction;
storyReactionPublicRepost#cfcd0f13 peer_id:Peer story:StoryItem = StoryReaction;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**storyReaction**](constructor/storyReaction) | How a certain peer reacted to a story |
| [**storyReactionPublicForward**](constructor/storyReactionPublicForward) | A certain peer has forwarded the story as a message to a public chat or channel |
| [**storyReactionPublicRepost**](constructor/storyReactionPublicRepost) | A certain peer has reposted the story |
## Banenkov Maxim

#### Contacts

* Email: bounderoll.23@gmail.com
* Telegram: [bounderoll](https://t.me/bounderoll)
* Vk: [Maxim Banenkov](https://vk.com/bounderoll)
* Discord: bounderoll#8351

#### About me

My goal in learning programming is to gain the necessary skills to provide two priorities that are important to me,
these are freedom and the ability to implement. I have no experience of working in companies, but I definitely have a
desire to grow, develop and move forward not only the computer mouse, but also the technological world. As my positive
traits, I can single out the ability to solve problems on my own, soft skills and an endless desire to move up

#### Skills

* HTML5
* CSS3: SCSS, Bootstrap, Material UI
* JavaScript: ES6+, TypeScript
* React: react-router, hooks, react-hook-form, axios
* Redux: react-redux, redux-thunk, redux-saga, reselect, immer
* React Native (basic)
* NodeJS: Express (basic)
* Package Managers: npm, yarn
* Methodologies: BEM
* Git (basic), GitHub
* Soft: Visual Studio Code, WebStorm
* DB: MongoDB (basic)

#### Code example

```
interface TweetProps {
    _id: string
    text: string
    createdAt: string
    images?: string[]
    user: {
        fullname: string
        username: string
        avatarUrl: string
    }
}

export const Tweet: React.FC<TweetProps> = ({_id, text, user, createdAt, images}: TweetProps): React.ReactElement => {
    const dispatch = useDispatch()
    const classes = useStylesHome()
    const history = useHistory()
    const [anchorEl, setAnchorEl] = useState<null | HTMLElement>(null)
    const open = Boolean(anchorEl)

    const handleClickTweet = (e: React.MouseEvent<HTMLAnchorElement>): void => {
        e.preventDefault()
        history.push(`/home/tweet/${_id}`)
    }

    const handleClick = (e: React.MouseEvent<HTMLElement>): void => {
        e.stopPropagation()
        e.preventDefault()
        setAnchorEl(e.currentTarget)
    }

    const handleClose = (e: React.MouseEvent<HTMLElement>): void => {
        e.stopPropagation()
        e.preventDefault()
        setAnchorEl(null)
    }

    const handleRemove = (e: React.MouseEvent<HTMLElement>): void => {
        handleClose(e)
        if (window.confirm('Вы действительно хотите удалить твит ?')) {
            dispatch(removeTweet(_id))
        }
    }

    return (
        <a onClick={handleClickTweet} className={classes.tweetWrapper} href={`/home/tweet/${_id}`}>
            <Paper className={classes.tweet} variant="outlined">
                <Avatar className={classes.tweetAvatar}
                        alt={`Аватар пользователя ${user.fullname}`}
                        src={user.avatarUrl}
                />
                <div className={classes.tweetBody}>
                    <div className={classes.tweetHeader}>
                        <div>
                            <b>{user.fullname}</b>&nbsp;
                            <span className={classes.tweetUserName}>@{user.username}</span>&nbsp;
                            <span className={classes.tweetUserName}>·</span>&nbsp;
                            <span className={classes.tweetUserName}>{formatDate(new Date(createdAt))}</span>
                        </div>
                        <div>
                            <IconButton aria-label="more"
                                        aria-controls="long-menu"
                                        aria-haspopup="true"
                                        onClick={handleClick}>
                                <MoreVertIcon/>
                            </IconButton>
                            <Menu anchorEl={anchorEl} open={open} onClose={handleClose}>
                                <MenuItem onClick={handleClose}>Редактировать</MenuItem>
                                <MenuItem onClick={handleRemove}>Удалить твит</MenuItem>
                            </Menu>
                        </div>
                    </div>
                    <Typography variant='body1' className={classes.tweetText} gutterBottom>
                        {text}
                        {images && <ImageList images={images}/>}
                    </Typography>
                </div>
            </Paper>
        </a>
    )
}
```

#### Experience

* 2021 (August 20-22) Digital Breakthrough Hackathon "Creative Industries. Communications and Content" 14th place
* 2021 (May 20) Digital wind "Thematic site" international stage 2nd place

Projects implemented during training are in my [GitHub account](https://github.com/bndroll) 

#### Education

2020 I entered SSTU, Institute of Applied Information Technologies, currently I am a 2nd year student

Courses
* Udemy [React Native](https://www.udemy.com/course/react-native-complete-guide)
* Udemy [JavaScript & React](https://www.udemy.com/course/javascript_full)

#### English

A2+
# Anilist-Mapping

`Anilist-Mapping` is a data mapping project that connects anime from `Anilist` to their corresponding streaming IDs on `Gogoanime`. This project provides a structured way to map and track anime across platforms using unique identifiers from Anilist and Gogoanime.

The data is organized in JSON files, each corresponding to an Anilist anime ID, and includes mapping information for Gogoanime's subtitled and dubbed versions.

## Project Structure

- Each anime is represented by a JSON file, with the filename being the **Anilist anime ID**.
- Each JSON file contains:
  - **id**: Anilist anime ID.
  - **mal-id**: The corresponding MyAnimeList ID (optional).
  - **url**: Link to the Anilist anime page.
  - **mapping**: Contains streaming details for Gogoanime.
    - **sub-id**: Gogoanime ID for the anime's subtitled version.
    - **dub-id**: Gogoanime ID for the anime's dubbed version.
    - **sub**: Flag indicating availability of the subtitled version.
    - **dub**: Flag indicating availability of the dubbed version.

### Example JSON Structure

```json
// data/1.json

{
    "id": 1,
    "mal-id": 1,
    "url": "https://anilist.co/anime/1",
    "mapping": {
        "gogoanime": {
            "sub": true,
            "dub": true,
            "sub-id": "cowboy-bebop",
            "dub-id": "cowboy-bebop-dub"
        }
    }
}

// This example represents Cowboy Bebop on Anilist and maps it to its subtitled and dubbed versions on Gogoanime.
```

## Purpose
The purpose of this project is to provide an easy way to link and map anime from Anilist to Gogoanime.

## Contributing
Contributions are welcome! Whether you're fixing an info, adding a new info, or improving the project in other ways, we encourage you to get involved.

## License
This project is licensed under [CC0 1.0 Universal](LICENSE)